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

- name: Backup DB and Node ID on source server
  hosts: lxpd194
  gather_facts: no
  any_errors_fatal: true
  become: yes
  become_user: postgres
  tasks:
    - name: Execute database backup script
      shell: bash ~postgres/backupnexusDB.bsh
      args:
        chdir: /tmp

    - name: Locate the newest database backup file
      find:
        paths: /opt/appdata/pgsql/backups
        patterns: "nexusdb2-*.bk"
      register: backup_files

    - name: Set facts for backup file path and name
      set_fact:
        latest_backup_path: "{{ (backup_files.files | sort(attribute='mtime') | last).path }}"
        backup_filename: "{{ (backup_files.files | sort(attribute='mtime') | last).path | basename }}"

    - name: Transfer database backup to target server via SCP
      command: scp -pr "{{ latest_backup_path }}" cmdeploy@lxpd211:

    - name: Compress Nexus Node ID keystores
      become_user: root
      command: tar -czvf /tmp/nexus-node-id.tar.gz -C /opt/appdata/nexus/sonatype-work/nexus3/keystores node
      args:
        chdir: /tmp

    - name: Set permissions for Node ID archive
      become_user: root
      file:
        path: /tmp/nexus-node-id.tar.gz
        mode: '0777'

    - name: Transfer Node ID archive to target server via SCP
      command: scp -pr /tmp/nexus-node-id.tar.gz cmdeploy@lxpd211:/tmp/

- name: Prepare DB and Node ID files on target server
  hosts: lxpd211
  gather_facts: no
  any_errors_fatal: true
  tasks:
    - name: Move database backup to tmp directory as cmdeploy
      command: cp "~/{{ hostvars['lxpd194']['backup_filename'] }}" /tmp/
      args:
        chdir: /tmp
      
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

    # - name: Extract Node ID archive
    #   become: yes
    #   command: tar -xzvf /tmp/nexus-node-id.tar.gz -C /opt/appdata/nexus/sonatype-work/nexus3/keystores
    #   args:
    #     chdir: /tmp
    
    # - name: Ensure correct ownership for restored Node ID
    #   become: yes
    #   file:
    #     path: /opt/appdata/nexus/sonatype-work/nexus3/keystores/node
    #     state: directory
    #     owner: nexus
    #     group: nexus
    #     recurse: yes

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
