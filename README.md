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

- name: Backup and direct transfer from source server
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
        backup_filename: "{{ (backup_files.files | sort(attribute='mtime') | last).path | basename }}"

    - name: Change permissions to 777 on source backup file
      become_user: postgres
      file:
        path: "/opt/appdata/pgsql/backups/{{ backup_filename }}"
        mode: '0777'

    - name: Direct SCP transfer to target server (Non-interactive)
      become_user: postgres
      command: scp -o StrictHostKeyChecking=no -o BatchMode=yes -pr "{{ backup_filename }}" cmdeploy@lxpd211:/tmp/
      args:
        chdir: /opt/appdata/pgsql/backups

- name: Prepare database file on target server
  hosts: lxpd211
  gather_facts: no
  any_errors_fatal: true
  tasks:
    - name: Set permissions on tmp database backup file
      file:
        path: "/tmp/{{ hostvars['lxpd194']['backup_filename'] }}"
        mode: '0777'

    - name: Move database backup to postgres home directory
      become: yes
      become_user: postgres
      command: cp "/tmp/{{ hostvars['lxpd194']['backup_filename'] }}" ~postgres/
      args:
        chdir: /tmp

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
