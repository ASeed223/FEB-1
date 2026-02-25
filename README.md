---
# =======================================================================
# [Commented Out] Step 1: Stop Nexus Application
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
# Step 2: Backup DB and Node ID on Source (lxpd194) and transfer to lxpd211
# =======================================================================
- hosts: lxpd194
  gather_facts: no
  any_errors_fatal: true
  become: yes
  become_user: postgres
  become_flags: "-i"
  vars:
    backup_dir: "/opt/appdata/pgsql/backups"
    node_archive: "/tmp/nexus-node-id.tar.gz"
    node_dir: "/opt/appdata/nexus/sonatype-work/nexus3/keystores/node"
    target_host: "lxpd211"
    target_user: "cmdeploy"
    target_db_dest: "/tmp"
    target_node_dest: "/tmp"
  tasks:
    - name: Run backup script
      shell: ./backupnexusDB.bsh
      args:
        chdir: "~"

    - name: Find backup files
      find:
        paths: "{{ backup_dir }}"
        patterns: "nexusdb2-*.bk"
        file_type: file
      register: backup_files

    - name: Fail if no backup file found
      fail:
        msg: "No backup file found in {{ backup_dir }}"
      when: backup_files.matched | int == 0

    - name: Set latest backup vars
      set_fact:
        latest_backup_path: "{{ (backup_files.files | sort(attribute='mtime') | last).path }}"
        backup_filename: "{{ (backup_files.files | sort(attribute='mtime') | last).path | basename }}"

    - name: Copy DB backup to target /tmp
      command: >
        scp -p "{{ latest_backup_path }}"
        "{{ target_user }}@{{ target_host }}:{{ target_db_dest }}/{{ backup_filename }}"

    - name: Create Node ID archive
      become_user: root
      command: >
        tar -czf "{{ node_archive }}"
        -C "{{ node_dir | dirname }}"
        "{{ node_dir | basename }}"

    - name: Set permissions on Node ID archive
      become_user: root
      file:
        path: "{{ node_archive }}"
        mode: "0644"

    - name: Copy Node ID archive to target /tmp
      command: >
        scp -p "{{ node_archive }}"
        "{{ target_user }}@{{ target_host }}:{{ target_node_dest }}/nexus-node-id.tar.gz"

# =======================================================================
# Step 3: Prepare DB and Node ID files on Target (lxpd211)
# =======================================================================
- hosts: lxpd211
  gather_facts: no
  any_errors_fatal: true
  vars:
    target_db_dest: "/tmp"
    target_node_archive: "/tmp/nexus-node-id.tar.gz"
  tasks:
    - name: Verify DB backup exists in /tmp
      stat:
        path: "{{ target_db_dest }}/{{ hostvars['lxpd194']['backup_filename'] }}"
      register: db_stat

    - name: Fail if DB backup missing in /tmp
      fail:
        msg: "DB backup not found: {{ target_db_dest }}/{{ hostvars['lxpd194']['backup_filename'] }}"
      when: not db_stat.stat.exists

    - name: Copy DB backup from /tmp to postgres home
      become: yes
      become_user: postgres
      become_flags: "-i"
      command: cp "{{ target_db_dest }}/{{ hostvars['lxpd194']['backup_filename'] }}" .

    - name: Verify Node ID archive exists in /tmp
      stat:
        path: "{{ target_node_archive }}"
      register: node_stat

    - name: Fail if Node ID archive missing in /tmp
      fail:
        msg: "Node ID archive not found: {{ target_node_archive }}"
      when: not node_stat.stat.exists

    # ===================================================================
    # [Commented Out] Restore Operations
    # ===================================================================
    # - name: Restore PostgreSQL database
    #   become: yes
    #   become_user: postgres
    #   become_flags: "-i"
    #   command: pg_restore -U postgres -d nexusdb2 --clean "~/{{ hostvars['lxpd194']['backup_filename'] }}"

    # - name: Extract Node ID archive
    #   become: yes
    #   command: tar -xzf "{{ target_node_archive }}" -C "/opt/appdata/nexus/sonatype-work/nexus3/keystores"

    # - name: Ensure correct ownership for restored Node ID
    #   become: yes
    #   file:
    #     path: "/opt/appdata/nexus/sonatype-work/nexus3/keystores/node"
    #     state: directory
    #     owner: nexus
    #     group: nexus
    #     recurse: yes

# =======================================================================
# [Commented Out] Step 5: Start Nexus Application
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
