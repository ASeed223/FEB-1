---
- name: Nexus HA Post-Upgrade Validation
  hosts: lxpd208, lxpd209
  gather_facts: no
  vars:
    # Service Configuration
    nexus_port: 8443
    nexus_scheme: "https"
    target_version: "3.89.0-09"
    
    # Path based on your HA configuration
    nexus_log_path: "/opt/nexus/sonatype-work/nexus3/log/nexus.log"

  tasks:
    # -------------------------------------------------------------------------
    # 1. NETWORK CONNECTIVITY
    # -------------------------------------------------------------------------
    - name: "[1/6] Wait for Nexus HTTPS port ({{ nexus_port }})"
      ansible.builtin.wait_for:
        port: "{{ nexus_port }}"
        host: "{{ inventory_hostname }}"
        state: started
        delay: 5
        timeout: 300
      register: port_check

    # -------------------------------------------------------------------------
    # 2. SYSTEM PROCESS CHECK
    # -------------------------------------------------------------------------
    - name: "[2/6] Verify Nexus Java process is active"
      ansible.builtin.shell: "ps -ef | grep java | grep nexus | grep -v grep"
      register: process_check
      changed_when: false

    # -------------------------------------------------------------------------
    # 3. APPLICATION HEALTH (API)
    # -------------------------------------------------------------------------
    - name: "[3/6] Validate System Status API (200 OK)"
      ansible.builtin.uri:
        url: "{{ nexus_scheme }}://localhost:{{ nexus_port }}/service/rest/v1/status"
        user: "{{ ansible_user }}"
        password: "{{ ansible_password }}"
        force_basic_auth: yes
        validate_certs: no
        method: GET
        status_code: 200
      register: api_status
      retries: 20
      delay: 10
      until: api_status.status == 200

    # -------------------------------------------------------------------------
    # 4. STORAGE INTEGRITY (WRITABLE)
    # -------------------------------------------------------------------------
    - name: "[4/6] Verify Blob Store is Writable"
      ansible.builtin.uri:
        url: "{{ nexus_scheme }}://localhost:{{ nexus_port }}/service/rest/v1/status/writable"
        user: "{{ ansible_user }}"
        password: "{{ ansible_password }}"
        force_basic_auth: yes
        validate_certs: no
        method: GET
        status_code: 200
      register: db_writable

    # -------------------------------------------------------------------------
    # 5. VERSION VERIFICATION (LOGS)
    # -------------------------------------------------------------------------
    - name: "[5/6] Confirm version {{ target_version }} in logs"
      ansible.builtin.shell: "grep 'Started Sonatype Nexus .* {{ target_version }}' {{ nexus_log_path }} | tail -n 1"
      register: log_version_check
      failed_when: log_version_check.stdout == ""
      changed_when: false

    # -------------------------------------------------------------------------
    # 6. RISK ASSESSMENT
    # -------------------------------------------------------------------------
    - name: "[6/6] Scan last 100 lines for ERROR logs"
      ansible.builtin.shell: "tail -n 100 {{ nexus_log_path }} | grep 'ERROR'"
      register: log_errors
      failed_when: false
      changed_when: false

    # -------------------------------------------------------------------------
    # SUMMARY REPORT
    # -------------------------------------------------------------------------
    - name: Display Validation Summary
      ansible.builtin.debug:
        msg:
          - "========================================================="
          - "  NEXUS UPGRADE VALIDATION REPORT"
          - "========================================================="
          - "Target Host    : {{ inventory_hostname }}"
          - "Target Version : {{ target_version }}"
          - "HTTPS Port     : UP ({{ nexus_port }})"
          - "API Health     : ONLINE (200 OK)"
          - "Storage Mode   : READ/WRITE (PASSED)"
          - "Log Version    : VERIFIED"
          - "Recent Errors  : {{ log_errors.stdout_lines | length }} errors found"
          - "========================================================="
