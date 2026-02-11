---
- name: Nexus_HA_Post-Upgrade Validation
  hosts: lxpd208,lxpd209
  gather_facts: no
  vars:
    # Service Configuration
    nexus_port: 8443
    nexus_scheme: "https"
    
    # Path based on your HA configuration
    test_artifact_path: "EDRRELEASE/gov/ca/ftb/app/accounting/AccountingCommon/maven-metadata.xml"

  tasks:
    # 1. NETWORK CONNECTIVITY
    - name: "[1/6] Wait for Nexus HTTPS port ({{ nexus_port }})"
      ansible.builtin.wait_for:
        port: "{{ nexus_port }}"
        host: "{{ inventory_hostname }}"
        state: started
        delay: 5
        timeout: 30
      register: port_check
      ignore_errors: yes

    # 2. SYSTEM PROCESS CHECK
    - name: "[2/6] Verify Nexus Java process is active"
      ansible.builtin.shell: "ps -ef | grep java | grep nexus | grep -v grep"
      register: process_check
      changed_when: false
      ignore_errors: yes

    # 3. APPLICATION HEALTH (API)
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
      retries: 5
      delay: 6
      until: api_status.status == 200
      ignore_errors: yes

    # 4. STORAGE INTEGRITY (WRITABLE)
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
      ignore_errors: yes

    # 5. FUNCTIONAL TEST: End-to-End Download Verification - lxpd208
    - name: "[5/5] Perform Test Download of an Artifact"
      ansible.builtin.uri:
        url: "https://lxpd208:8443/repository/{{ test_artifact_path }}"
        user: "{{ ansible_user }}"
        password: "{{ ansible_password }}"
        force_basic_auth: yes
        validate_certs: no
        method: GET
        status_code: 200
      register: download_test_lxpd208
      # File is fetched into memory and discarded to verify readability without disk clutter
      ignore_errors: yes

      # 6. FUNCTIONAL TEST: End-to-End Download Verification - lxpd209
    - name: "[5/5] Perform Test Download of an Artifact"
      ansible.builtin.uri:
        url: "https://lxpd209:8443/repository/{{ test_artifact_path }}"
        user: "{{ ansible_user }}"
        password: "{{ ansible_password }}"
        force_basic_auth: yes
        validate_certs: no
        method: GET
        status_code: 200
      register: download_test_lxpd209
      # File is fetched into memory and discarded to verify readability without disk clutter
      ignore_errors: yes


    - name: "DisplayFinal Validation Summary"
      ansible.builtin.debug:
            msg:
              - "========================================================="
              - "  NEXUS HA VALIDATION REPORT"
              - "========================================================="
              - "Target Host    : {{ inventory_hostname }}"
              - "HTTPS Port     : {{ 'UP' if not port_check.failed else 'DOWN' }} ({{ nexus_port }})"
              - "System Status  : {{ 'PASSED' if api_status.status == 200 else 'FAILED (' ~ api_status.status | default('No Response') ~ ')' }}"
              - "Storage Write  : {{ 'PASSED' if db_writable.status == 200 else 'FAILED' }}"
              - "Download Test  : {{ 'PASSED' if download_test_lxpd208.status == 200 else 'FAILED' }}"
              - "Download Test  : {{ 'PASSED' if download_test_lxpd209.status == 200 else 'FAILED' }}"
              - "========================================================="
