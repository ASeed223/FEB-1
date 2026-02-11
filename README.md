---
- name: Nexus_HA_Post-Upgrade Validation
  hosts: lxpd208, lxpd209
  gather_facts: no
  vars:
    nexus_port: 8443
    nexus_scheme: "https"
    # Unified test path
    test_artifact_path: "EDRRELEASE/gov/ca/ftb/app/accounting/AccountingCommon/maven-metadata.xml"

  tasks:
    # -------------------------------------------------------------------------
    # 1. Connectivity: Wait for the port to open
    # -------------------------------------------------------------------------
    - name: "[1/5] Wait for Nexus HTTPS port"
      ansible.builtin.wait_for:
        port: "{{ nexus_port }}"
        host: "{{ inventory_hostname }}"
        state: started
        delay: 5
        timeout: 600  # Increased to 10 mins for 2.8TB data metadata check
      register: port_check
      ignore_errors: yes

    # -------------------------------------------------------------------------
    # 2. Process: Check if Java is actually running
    # -------------------------------------------------------------------------
    - name: "[2/5] Verify Nexus Java process"
      ansible.builtin.shell: "ps -ef | grep java | grep nexus | grep -v grep"
      register: process_check
      changed_when: false
      ignore_errors: yes

    # -------------------------------------------------------------------------
    # 3. API Health: Check basic service response
    # -------------------------------------------------------------------------
    - name: "[3/5] Validate System Status API"
      ansible.builtin.uri:
        url: "{{ nexus_scheme }}://localhost:{{ nexus_port }}/service/rest/v1/status"
        user: "{{ ansible_user }}"
        password: "{{ ansible_password }}"
        force_basic_auth: yes
        validate_certs: no
        method: GET
      register: api_status
      retries: 40      # 40 * 15s = 10 minutes total waiting time
      delay: 15
      until: api_status.status == 200
      ignore_errors: yes

    # -------------------------------------------------------------------------
    # 4. Storage: Verify Blob Store is Writable
    # -------------------------------------------------------------------------
    - name: "[4/5] Verify Blob Store is Writable"
      ansible.builtin.uri:
        url: "{{ nexus_scheme }}://localhost:{{ nexus_port }}/service/rest/v1/status/writable"
        user: "{{ ansible_user }}"
        password: "{{ ansible_password }}"
        force_basic_auth: yes
        validate_certs: no
        method: GET
      register: db_writable
      ignore_errors: yes

    # -------------------------------------------------------------------------
    # 5. Functional: Download test from the current host
    # -------------------------------------------------------------------------
    - name: "[5/5] Perform Local Download Test"
      ansible.builtin.uri:
        url: "{{ nexus_scheme }}://localhost:{{ nexus_port }}/repository/{{ test_artifact_path }}"
        user: "{{ ansible_user }}"
        password: "{{ ansible_password }}"
        force_basic_auth: yes
        validate_certs: no
        method: GET
      register: download_test
      ignore_errors: yes

    # -------------------------------------------------------------------------
    # FINAL SUMMARY REPORT
    # -------------------------------------------------------------------------
    - name: "Display Final Validation Summary"
      ansible.builtin.debug:
        msg:
          - "========================================================="
          - "  NEXUS HA VALIDATION REPORT ({{ inventory_hostname }})"
          - "========================================================="
          - "Node Name      : {{ inventory_hostname }}"
          - "HTTPS Port     : {{ 'UP' if not (port_check.failed | default(false)) else 'DOWN' }}"
          - "Java Process   : {{ 'RUNNING' if process_check.rc == 0 else 'NOT FOUND' }}"
          - "API Status     : {{ 'PASSED' if api_status.status == 200 else 'FAILED (' ~ (api_status.status | default('No Resp')) ~ ')' }}"
          - "Storage Write  : {{ 'PASSED' if db_writable.status == 200 else 'FAILED' }}"
          - "Download Test  : {{ 'PASSED' if download_test.status == 200 else 'FAILED' }}"
          - "========================================================="
