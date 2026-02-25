---
# =======================================================================
# Step 1: Stop Nexus Application (commented out for testing)
# =======================================================================
# - hosts: lxpd208,lxpd209
#   gather_facts: no
#   any_errors_fatal: true
#   become: yes
#   tasks:
#     - name: Stop nexus service
#       systemd:
#         name: nexus
#         state: stopped

# =======================================================================
# Step 2: Backup DB on Source Server (lxpd194) and copy to lxpd211
# =======================================================================
- hosts: lxpd194
  gather_facts: no
  any_errors_fatal: true
  become: yes
  become_user: postgres
  vars:
    current_date: "{{ lookup('pipe', 'date +%Y-%m-%d') }}"
    target_filename: "nexusdb2-{{ current_date }}.bk"
    backup_dir: "{{ lookup('env', 'HOME') }}/backups"
  tasks:
    - name: Run backup script
      shell: ./backupnexusDB.bsh
      args:
        chdir: "{{ lookup('env', 'HOME') }}"

    - name: Find backup files
      find:
        paths: "{{ backup_dir }}"
        patterns: "nexusdb2-*.bk"
      register: backup_files

    - name: Fail if no backup file found
      fail:
        msg: "No backup file found in {{ backup_dir }}"
      when: backup_files.matched | int == 0

    - name: Set latest backup path
      set_fact:
        latest_backup: "{{ (backup_files.files | sort(attribute='mtime') | last).path }}"

    - name: Rename backup to expected filename
      command: mv "{{ latest_backup }}" "{{ backup_dir }}/{{ target_filename }}"

    - name: Set permissions on backup file
      file:
        path: "{{ backup_dir }}/{{ target_filename }}"
        mode: "0644"

    - name: Copy backup to lxpd211 (to cmdeploy home)
      command: scp -p "{{ backup_dir }}/{{ target_filename }}" "cmdeploy@lxpd211:{{ target_filename }}"

# =======================================================================
# Step 3: Prepare DB file on Target Server (lxpd211)
# =======================================================================
- hosts: lxpd211
  gather_facts: no
  any_errors_fatal: true
  vars:
    current_date: "{{ lookup('pipe', 'date +%Y-%m-%d') }}"
    target_filename: "nexusdb2-{{ current_date }}.bk"
  tasks:
    - name: Verify backup exists in cmdeploy home
      stat:
        path: "{{ lookup('env', 'HOME') }}/{{ target_filename }}"
      register: bk_stat

    - name: Fail if backup is missing
      fail:
        msg: "Backup file not found in cmdeploy home: {{ target_filename }}"
      when: not bk_stat.stat.exists

    - name: Copy backup to /tmp
      command: cp "{{ lookup('env', 'HOME') }}/{{ target_filename }}" "/tmp/{{ target_filename }}"

    - name: Set permissions on /tmp backup file
      file:
        path: "/tmp/{{ target_filename }}"
        mode: "0644"

    - name: Copy backup from /tmp to postgres home
      become: yes
      become_user: postgres
      command: cp "/tmp/{{ target_filename }}" "{{ lookup('env', 'HOME') }}/{{ target_filename }}"

    # Restore is intentionally commented out
    # - name: Restore database
    #   become: yes
    #   become_user: postgres
    #   command: pg_restore -U postgres -d nexusdb --clean "{{ lookup('env', 'HOME') }}/{{ target_filename }}"

# =======================================================================
# Step 4: Start Nexus Application (commented out for testing)
# =======================================================================
# - hosts: lxpd208,lxpd209
#   gather_facts: no
#   any_errors_fatal: true
#   become: yes
#   tasks:
#     - name: Start nexus service
#       systemd:
#         name: nexus
#         state: started
