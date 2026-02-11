---
- name: Nexus HA Post-Upgrade Business Validation
  hosts: lxpd208, lxpd209
  gather_facts: no
  vars:
    # Service settings
    nexus_port: 8443
    nexus_scheme: "https"
    
    # ACTION REQUIRED: Update this to a real file path in your Nexus (e.g., .xml, .pom, or .jar)
    test_artifact_path: "repository/maven-public/org/apache/maven/maven-model/3.0/maven-metadata.xml"

  tasks:
    # -------------------------------------------------------------------------
    # 1. CONNECTIVITY: Ensure the HTTPS port is listening
    # -------------------------------------------------------------------------
    - name: "[1/5] Wait for Nexus HTTPS port ({{ nexus_port }})"
      ansible.builtin.wait_for:
        port: "{{ nexus_port }}"
        host: "{{ inventory_hostname }}"
        state: started
        delay: 5
        timeout: 600  # 10 min timeout to allow for Database Migration
      register: port_check

    # -------------------------------------------------------------------------
    # 2. SYSTEM PROCESS CHECK
    # -------------------------------------------------------------------------
    - name: "[2/6] Verify Nexus Java process is active"
      ansible.builtin.shell: "ps -ef | grep java | grep nexus | grep -v grep"
      register: process_check
      changed_when: false
    # -------------------------------------------------------------------------
    # 3. STORAGE HEALTH: Ensure the 2.8TB Blob Store is mounted and Writable
    # -------------------------------------------------------------------------
    - name: "[3/5] Verify Blob Store is Writable"
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
    # 4. REPOSITORY STATUS: Ensure key repositories are Online
    # -------------------------------------------------------------------------
    - name: "[4/5] Ensure Repositories are ONLINE"
      ansible.builtin.uri:
        url: "{{ nexus_scheme }}://localhost:{{ nexus_port }}/service/rest/v1/repositories"
        user: "{{ ansible_user }}"
        password: "{{ ansible_password }}"
        force_basic_auth: yes
        validate_certs: no
        method: GET
        return_content: yes
      register: repo_list
      failed_when: "'online' not in repo_list.content"

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
