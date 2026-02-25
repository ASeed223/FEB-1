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

- name: Backup and direct transfer from source to target
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

    - name: Set facts for the latest backup
      become_user: postgres
      set_fact:
        latest_backup_path: "{{ (backup_files.files | sort(attribute='mtime') | last).path }}"
        backup_filename: "{{ (backup_files.files | sort(attribute='mtime') | last).path | basename }}"

    - name: Direct SCP from lxpd194 to lxpd211
      become_user: postgres
      # This requires SSH keys to be set up between postgres@lxpd194 and cmdeploy@lxpd211
      command: scp -pr "{{ latest_backup_path }}" cmdeploy@lxpd211:
      args:
        chdir: /tmp

    - name: Cleanup old backups on source server (keep only latest)
      become_user: postgres
      shell: "find /opt/appdata/pgsql/backups -name 'nexusdb2-*.bk' ! -name '{{ backup_filename }}' -delete"
      args:
        chdir: /tmp

- name: Prepare database file on target server
  hosts: lxpd211
  gather_facts: no
  any_errors_fatal: true
  tasks:
    - name: Move database backup to tmp directory as cmdeploy
      # File arrives in cmdeploy home via SCP
      command: cp "~/{{ hostvars['lxpd194']['backup_filename'] }}" /tmp/
      args:
        chdir: /tmp
      
    - name: Set permissions on tmp backup file
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
