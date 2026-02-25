---
# - name: Stop Nexus application
#   hosts: lxpd208, lxpd209
#   gather_facts: no
#   any_errors_fatal: true
#   become: yes
#   tasks:
#     - name: Stop nexus service
#       systemd:
#         name: nexus
#         state: stopped

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

- name: Prepare database file on target server
  hosts: lxpd211
  gather_facts: no
  any_errors_fatal: true
  tasks:
    # Upload from Ansible controller to lxpd211 /tmp
    - name: Copy database backup to target server tmp
      copy:
        src: "/tmp/{{ hostvars['lxpd194']['backup_filename'] }}"
        dest: "/tmp/{{ hostvars['lxpd194']['backup_filename'] }}"
        mode: '0777'

    - name: Move database backup to postgres home directory
      become: yes
      become_user: postgres
      command: cp "/tmp/{{ hostvars['lxpd194']['backup_filename'] }}" ~postgres/
      args:
        chdir: /tmp

    # 自动清理 Ansible 本地的临时文件
    - name: Clean up temporary backup file on Ansible controller
      delegate_to: localhost
      run_once: true
      file:
        path: "/tmp/{{ hostvars['lxpd194']['backup_filename'] }}"
        state: absent

    # - name: Restore PostgreSQL database
    #   become: yes
    #   become_user: postgres
    #   command: pg_restore -U postgres -d nexusdb --clean "~postgres/{{ hostvars['lxpd194']['backup_filename'] }}"
    #   args:
    #     chdir: /tmp

# - name: Start Nexus application
#   hosts: lxpd208, lxpd209
#   gather_facts: no
#   any_errors_fatal: true
#   become: yes
#   tasks:
#     - name: Start nexus service
#       systemd:
#         name: nexus
#         state: started
