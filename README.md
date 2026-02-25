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

    # Use 'fetch' to download from lxpd194 to Ansible controller
    - name: Fetch database backup to Ansible controller
      become_user: postgres
      fetch:
        src: "{{ latest_backup_path }}"
        dest: "/tmp/{{ backup_filename }}"
        flat: yes

    - name: Compress Nexus Node ID keystores
      become_user: root
      command: tar -czvf /tmp/nexus-node-id.tar.gz -C /opt/appdata/nexus/sonatype-work/nexus3/keystores node
      args:
        chdir: /tmp

    # Use 'fetch' to download Node ID archive to Ansible controller
    - name: Fetch Node ID archive to Ansible controller
      become_user: root
      fetch:
        src: /tmp/nexus-node-id.tar.gz
        dest: /tmp/nexus-node-id.tar.gz
        flat: yes

- name: Prepare DB and Node ID files on target server
  hosts: lxpd211
  gather_facts: no
  any_errors_fatal: true
  tasks:
    # Use 'copy' to upload from Ansible controller to lxpd211
    - name: Copy database backup to target server tmp
      copy:
        src: "/tmp/{{ hostvars['lxpd194']['backup_filename'] }}"
        dest: "/tmp/{{ hostvars['lxpd194']['backup_filename'] }}"
        mode: '0777'

    - name: Copy Node ID archive to target server tmp
      copy:
        src: /tmp/nexus-node-id.tar.gz
        dest: /tmp/nexus-node-id.tar.gz
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
    #   become_user: root
    #   command: tar -xzvf /tmp/nexus-node-id.tar.gz -C /opt/appdata/nexus/sonatype-work/nexus3/keystores
    #   args:
    #     chdir: /tmp
    
    # - name: Ensure correct ownership for restored Node ID
    #   become: yes
    #   become_user: root
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
