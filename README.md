- name: Prepare and Restore database on target server
  hosts: lxpd211
  gather_facts: no
  any_errors_fatal: true
  become: yes
  tasks:
    - name: Set permissions on tmp database backup file
      file:
        path: "/tmp/{{ hostvars['lxpd194']['backup_filename'] }}"
        mode: '0777'

    - name: Move database backup to postgres home directory
      become_user: postgres
      command: cp "/tmp/{{ hostvars['lxpd194']['backup_filename'] }}" ~postgres/
      args:
        chdir: /tmp
      
    - name: Force disconnect any active connections to nexusdb
      become_user: postgres
      command: psql -c "SELECT pg_terminate_backend(pid) FROM pg_stat_activity WHERE datname = 'nexusdb' AND pid <> pg_backend_pid();"
      ignore_errors: yes 

    - name: Drop existing dirty nexusdb
      become_user: postgres
      command: dropdb --if-exists nexusdb

    - name: Create fresh empty nexusdb
      become_user: postgres
      command: createdb -O nexdbuser nexusdb

    - name: Restore PostgreSQL database
      become_user: postgres
      command: pg_restore -U postgres -d nexusdb "~postgres/{{ hostvars['lxpd194']['backup_filename'] }}"
