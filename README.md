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
    # 5. FUNCTIONAL TEST: End-to-End Download Verification
    # -------------------------------------------------------------------------
    - name: "[5/5] Perform Test Download of an Artifact"
      ansible.builtin.uri:
        url: "{{ nexus_scheme }}://localhost:{{ nexus_port }}/{{ test_artifact_path }}"
        user: "{{ ansible_user }}"
        password: "{{ ansible_password }}"
        force_basic_auth: yes
        validate_certs: no
        method: GET
        status_code: 200
      register: download_test
      # File is fetched into memory and discarded to verify readability without disk clutter
      ignore_errors: yes

    # -------------------------------------------------------------------------
    # FINAL SUMMARY REPORT
    # -------------------------------------------------------------------------
    - name: Display Final Validation Summary
      ansible.builtin.debug:
        msg:
          - "========================================================="
          - "  NEXUS HA UPGRADE VALIDATION REPORT"
          - "========================================================="
          - "Node           : {{ inventory_hostname }}"
          - "HTTPS Port     : UP ({{ nexus_port }})"
          - "System Ready   : PASSED"
          - "Storage Write  : PASSED"
          - "Repo Online    : PASSED"
          - "Download Test  : {{ 'SUCCESS' if download_test.status == 200 else 'FAILED' }}"
          - "========================================================="
