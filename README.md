---
- name: Nexus HA Post-Upgrade Validation
  hosts: lxpd208, lxpd209
  gather_facts: no
  vars:
    # Uses variables defined in your inventory
    nexus_port: 8443
    nexus_scheme: "https"
    # Path based on your HA configuration
    nexus_log: "/opt/nexus/sonatype-work/nexus3/log/nexus.log"
    target_version: "3.89.0-09"

  tasks:
    # 1. Connectivity Check
    - name: Wait for Nexus HTTPS port ({{ nexus_port }})
      wait_for:
        port: "{{ nexus_port }}"
        host: "{{ inventory_hostname }}"
        state: started
        delay: 5
        timeout: 300
      register: port_check

    # 2. Process Check
    - name: Verify Java process is running
      shell: "ps -ef | grep java | grep nexus | grep -v grep"
      register: process_check
      changed_when: false

    # 3. Service Health Check (API)
    - name: Validate API Health Status (200 OK)
      uri:
        url: "{{ nexus_scheme }}://localhost:{{ nexus_port }}/service/rest/v1/status"
        user: "{{ nexus_user }}"
        password: "{{ nexus_password }}"
        force_basic_auth: yes
        validate_certs: no
        method: GET
        status_code: 200
      register: api_status
      retries: 20
      delay: 10
      until: api_status.status == 200

    # 4. Storage Writable Check
    - name: Verify Blob Store is Writable
      uri:
        url: "{{ nexus_scheme }}://localhost:{{ nexus_port }}/service/rest/v1/status/writable"
        user: "{{ nexus_user }}"
        password: "{{ nexus_password }}"
        force_basic_auth: yes
        validate_certs: no
        method: GET
        status_code: 200
      register: db_writable

    # 5. Log Verification
    - name: Confirm version {{ target_version }} in logs
      shell: "grep 'Started Sonatype Nexus .* {{ target_version }}' {{ nexus_log }} | tail -n 1"
      register: log_version_check
      failed_when: log_version_check.stdout == ""
      changed_when: false

    # 6. Risk Assessment
    - name: Scan last 100 lines for ERRORs
      shell: "tail -n 100 {{ nexus_log }} | grep 'ERROR'"
      register: log_errors
      failed_when: false
      changed_when: false

    # Final Summary Output
    - name: Display Validation Summary
      debug:
        msg:
          - "============================================="
          - "Nexus Upgrade Validation: {{ 'SUCCESS' if log_version_check.rc == 0 else 'FAILED' }}"
          - "============================================="
          - "Node           : {{ inventory_hostname }}"
          - "Port 8443      : UP"
          - "API Status     : ONLINE"
          - "Storage Mode   : READ/WRITE"
          - "Log Version    : VERIFIED"
          - "Recent Errors  : {{ log_errors.stdout_lines | length }} found"
          - "============================================="
