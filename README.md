- name: Stop Nexus HA 01 on lxpd208
  hosts: lxpd208
  gather_facts: no
  any_errors_fatal: true
  tasks:
    - name: Check if Nexus is currently running
      ansible.builtin.shell: ps -ef | grep java | grep "/opt/nexus/nexus" | grep -v grep
      register: initial_process_check
      # grep returns 0 if process exists, 1 if not found. We don't want to fail here.
      failed_when: false
      changed_when: false

    - name: Stop Nexus HA 01
      ansible.builtin.shell: /opt/nexus/nexus/bin/nexus stop
      register: stop_result
      # Only run if the initial check found the process
      when: initial_process_check.rc == 0
      failed_when: 
        - stop_result.rc != 0 
        - '"PID file not found" not in stop_result.stdout'
      changed_when: stop_result.rc == 0

    - name: Verify Nexus is completely stopped (Retry for 1 minute)
      ansible.builtin.shell: ps -ef | grep java | grep "/opt/nexus/nexus" | grep -v grep
      register: verify_stop
      # Loop until rc is NOT 0 (meaning grep failed to find the process, so it is stopped)
      until: verify_stop.rc != 0
      retries: 12
      delay: 5
      changed_when: false
      # KEY FIX: Use failed_when: false instead of ignore_errors.
      # This prevents the red "fatal" error when grep returns 1 (not found).
      failed_when: false

    - name: Fail if Nexus HA 01 is still running
      ansible.builtin.fail:
        msg: "Nexus HA 01 is still running on lxpd208!"
      # If verify_stop.rc is still 0, it means grep still found the process
      when: verify_stop.rc == 0

- name: Stop Nexus HA 02 on lxpd209
  hosts: lxpd209
  gather_facts: no
  any_errors_fatal: true
  tasks:
    - name: Check if Nexus is currently running (Process check)
      ansible.builtin.shell: ps -ef | grep java | grep "/opt/nexus/nexus" | grep -v grep
      register: initial_process_check
      # grep returns 0 if process exists, 1 if not found. We don't want to fail here.
      failed_when: false
      changed_when: false

    - name: Stop Nexus HA 02 (Only if running)
      ansible.builtin.shell: /opt/nexus/nexus/bin/nexus stop
      register: stop_result
      # Only run if the initial check found the process
      when: initial_process_check.rc == 0
      failed_when: 
        - stop_result.rc != 0 
        - '"PID file not found" not in stop_result.stdout'
      changed_when: stop_result.rc == 0

    - name: Verify Nexus is completely stopped (Retry for 1 minute)
      ansible.builtin.shell: ps -ef | grep java | grep "/opt/nexus/nexus" | grep -v grep
      register: verify_stop
      until: verify_stop.rc != 0
      retries: 12
      delay: 5
      changed_when: false
      failed_when: false

    - name: Fail if Nexus HA 02 is still running
      ansible.builtin.fail:
        msg: "Nexus HA 02 is still running on lxpd209!"
      # If verify_stop.rc is still 0, it means grep still found the process
      when: verify_stop.rc == 0

- name: Backup database on source server
  hosts: lxpd194
  gather_facts: no
  any_errors_fatal: true
  become: yes
  tasks:
    - name: Execute database backup script
      become_user: postgres
      shell: bash ~postgres/backupnexusDB.bsh
      args:
        chdir: /tmp

    - name: Locate the newest database backup file
      become_user: postgres
      find:
        paths: /opt/appdata/pgsql/backups
        patterns: "nexusdb2-*.bk"
      register: backup_files

    - name: Set facts for backup file path and name
      become_user: postgres
      set_fact:
        latest_backup_path: "{{ (backup_files.files | sort(attribute='mtime') | last).path }}"
        backup_filename: "{{ (backup_files.files | sort(attribute='mtime') | last).path | basename }}"

    # Download from lxpd194 to Ansible controller /tmp
    - name: Fetch database backup to Ansible controller
      become_user: postgres
      fetch:
        src: "{{ latest_backup_path }}"
        dest: "/tmp/{{ backup_filename }}"
        flat: yes

- name: Prepare and Restore database on target server
  hosts: lxpd211
  gather_facts: no
  any_errors_fatal: true
  become: yes
  become_user: postgres
  tasks:
    - name: Copy database backup from Ansible controller to postgres home directory
      copy:
        src: "/tmp/{{ hostvars['lxpd194']['backup_filename'] }}"
        dest: "~postgres/{{ hostvars['lxpd194']['backup_filename'] }}"
        mode: '0600'

    - name: Force disconnect any active connections to nexusdb
      command: psql -c "SELECT pg_terminate_backend(pid) FROM pg_stat_activity WHERE datname = 'nexusdb' AND pid <> pg_backend_pid();"
      ignore_errors: yes

    - name: Drop existing dirty nexusdb
      command: dropdb --if-exists nexusdb

    - name: Create fresh empty nexusdb
      command: createdb -O nexdbuser nexusdb

    - name: Restore PostgreSQL database
      command: pg_restore -U postgres -d nexusdb "~postgres/{{ hostvars['lxpd194']['backup_filename'] }}"

    - name: Clean up temporary backup file on Ansible controller
      delegate_to: localhost
      run_once: true
      file:
        path: "/tmp/{{ hostvars['lxpd194']['backup_filename'] }}"
        state: absent


- name: Start Nexus HA 01 on lxpd208 with Auto-Heal
  hosts: lxpd208
  gather_facts: no
  any_errors_fatal: true
  tasks:
    # 1. PRE-CHECK: Use API to see if the service is already UP
    - name: Pre-check - Check if Nexus API is accessible (HTTP 200)
      ansible.builtin.shell: >
        curl -k -s -o /dev/null -w "%{http_code}" https://127.0.0.1:8443/service/rest/v1/status
      register: pre_check
      # Ignore error if site is down (curl might fail)
      failed_when: false
      changed_when: false

    - name: Display status if Nexus is already running
      ansible.builtin.debug:
        msg: "Nexus is currently running and accessible (HTTP 200). Skipping start tasks."
      when: pre_check.stdout == "200"

    # 2. INITIAL START (If pre-check failed)
    - name: Start Nexus HA 01 (First Attempt)
      ansible.builtin.shell: /opt/nexus/nexus/bin/nexus start
      register: start_result_1
      # Only run if pre-check was NOT 200
      when: pre_check.stdout != "200"
      failed_when: start_result_1.rc != 0
      changed_when: start_result_1.rc == 0

    - name: Verify Nexus API is Ready (Wait up to 1 min)
      ansible.builtin.shell: >
        curl -k -s -o /dev/null -w "%{http_code}" https://127.0.0.1:8443/service/rest/v1/status
      register: verify_run_1
      # Keep retrying until output is exactly "200"
      until: verify_run_1.stdout == "200"
      retries: 12  # 12 attempts x 5 seconds = 60 seconds
      delay: 5
      # Do not fail yet; allow the recovery step to run
      failed_when: false
      changed_when: false
      when: pre_check.stdout != "200"

    # 3. AUTO-HEAL: Restart if initial verification failed
    - name: RECOVERY - Force Stop Nexus (If initial verification failed)
      ansible.builtin.shell: /opt/nexus/nexus/bin/nexus stop
      register: stop_recovery
      # Ignore stop errors (goal is to clear the state)
      failed_when: false
      when: 
        - pre_check.stdout != "200" 
        - verify_run_1.stdout != "200"

    - name: RECOVERY - Start Nexus Again
      ansible.builtin.shell: /opt/nexus/nexus/bin/nexus start
      register: start_result_2
      when: 
        - pre_check.stdout != "200" 
        - verify_run_1.stdout != "200"

    - name: RECOVERY - Verify API Again (Wait up to 1 min)
      ansible.builtin.shell: >
        curl -k -s -o /dev/null -w "%{http_code}" https://127.0.0.1:8443/service/rest/v1/status
      register: verify_run_2
      until: verify_run_2.stdout == "200"
      retries: 12
      delay: 5
      failed_when: false
      changed_when: false
      when: 
        - pre_check.stdout != "200" 
        - verify_run_1.stdout != "200"

    # 4. FINAL CHECK: Fail if still not ready after all attempts
    - name: Final Failure Check
      ansible.builtin.fail:
        msg: "Nexus HA 01 failed to start on lxpd208 after retry! API did not return 200."
      when: 
        - pre_check.stdout != "200"
        - verify_run_1.stdout != "200"
        - verify_run_2.stdout != "200"

- name: Start Nexus HA 02 on lxpd209 with Auto-Heal
  hosts: lxpd209
  gather_facts: no
  any_errors_fatal: true
  tasks:
    # 1. PRE-CHECK: Use API to see if the service is already UP
    - name: Pre-check - Check if Nexus API is accessible (HTTP 200)
      ansible.builtin.shell: >
        curl -k -s -o /dev/null -w "%{http_code}" https://127.0.0.1:8443/service/rest/v1/status
      register: pre_check
      # Ignore error if site is down (curl might fail)
      failed_when: false
      changed_when: false

    - name: Display status if Nexus is already running
      ansible.builtin.debug:
        msg: "Nexus is currently running and accessible (HTTP 200). Skipping start tasks."
      when: pre_check.stdout == "200"

    # 2. INITIAL START (If pre-check failed)
    - name: Start Nexus HA 02 (First Attempt)
      ansible.builtin.shell: /opt/nexus/nexus/bin/nexus start
      register: start_result_1
      # Only run if pre-check was NOT 200
      when: pre_check.stdout != "200"
      failed_when: start_result_1.rc != 0
      changed_when: start_result_1.rc == 0

    - name: Verify Nexus API is Ready (Wait up to 1 min)
      ansible.builtin.shell: >
        curl -k -s -o /dev/null -w "%{http_code}" https://127.0.0.1:8443/service/rest/v1/status
      register: verify_run_1
      # Keep retrying until output is exactly "200"
      until: verify_run_1.stdout == "200"
      retries: 12  # 12 attempts x 5 seconds = 60 seconds
      delay: 5
      # Do not fail yet; allow the recovery step to run
      failed_when: false
      changed_when: false
      when: pre_check.stdout != "200"

    # 3. AUTO-HEAL: Restart if initial verification failed
    - name: RECOVERY - Force Stop Nexus (If initial verification failed)
      ansible.builtin.shell: /opt/nexus/nexus/bin/nexus stop
      register: stop_recovery
      # Ignore stop errors (goal is to clear the state)
      failed_when: false
      when: 
        - pre_check.stdout != "200" 
        - verify_run_1.stdout != "200"

    - name: RECOVERY - Start Nexus Again
      ansible.builtin.shell: /opt/nexus/nexus/bin/nexus start
      register: start_result_2
      when: 
        - pre_check.stdout != "200" 
        - verify_run_1.stdout != "200"

    - name: RECOVERY - Verify API Again (Wait up to 1 min)
      ansible.builtin.shell: >
        curl -k -s -o /dev/null -w "%{http_code}" https://127.0.0.1:8443/service/rest/v1/status
      register: verify_run_2
      until: verify_run_2.stdout == "200"
      retries: 12
      delay: 5
      failed_when: false
      changed_when: false
      when: 
        - pre_check.stdout != "200" 
        - verify_run_1.stdout != "200"

    # 4. FINAL CHECK: Fail if still not ready after all attempts
    - name: Final Failure Check
      ansible.builtin.fail:
        msg: "Nexus HA 02 failed to start on lxpd209 after retry! API did not return 200."
      when: 
        - pre_check.stdout != "200"
        - verify_run_1.stdout != "200"
        - verify_run_2.stdout != "200"
