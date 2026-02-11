---
- name: Nexus HA Post-Upgrade Functional Validation
  hosts: lxpd208, lxpd209
  gather_facts: no
  vars:
    # Service settings
    nexus_port: 8443
    nexus_scheme: "https"
    
    # Update this path to a real small file existing in your Nexus
    test_artifact_path: "repository/maven-public/org/apache/maven/maven-model/3.0/maven-model-3.0.jar"

  tasks:
    # -------------------------------------------------------------------------
    # 1. Connectivity: Ensure the HTTPS port is listening
    # -------------------------------------------------------------------------
    - name: "[1/5] Wait for Nexus HTTPS port ({{ nexus_port }})"
      ansible.builtin.wait_for:
        port: "{{ nexus_port }}"
        host: "{{ inventory_hostname }}"
        state: started
        delay: 5
        timeout: 600  # 10 minutes timeout for database migration
      register: port_check

    # -------------------------------------------------------------------------
    # 2. System Ready: Check if the application has finished initializing
    # -------------------------------------------------------------------------
    - name: "[2/5] Validate System Ready Status"
      ansible.builtin.uri:
        url: "{{ nexus_scheme }}://localhost:{{ nexus_port }}/service/rest/v1/status/ready"
        user: "{{ ansible_user }}"
        password: "{{ ansible_password }}"
        force_basic_auth: yes
        validate_certs: no
        method: GET
        status_code: 200
      register: ready_result
      retries: 30
      delay: 20
      until: ready_result.status == 200

    # -------------------------------------------------------------------------
    # 3. Storage Health: Verify the 2.8TB Blob Store is not Read-Only
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

    # -------------------------------------------------------------------------
    # 4. Repository Check: Ensure repositories are Online
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
    # 5. Functional Test: Try to download an actual file
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
      ignore_errors: yes

    # -------------------------------------------------------------------------
    # SUMMARY
    # -------------------------------------------------------------------------
    - name: Display Validation Results
      ansible.builtin.debug:
        msg:
          - "========================================================="
          - "  NEXUS HA UPGRADE VALIDATION REPORT"
          - "========================================================="
          - "Node           : {{ inventory_hostname }}"
          - "Port 8443 Status: UP"
          - "System Ready   : PASSED"
          - "Storage Write  : PASSED"
          - "Repo Online    : PASSED"
          - "Download Test  : {{ 'SUCCESS' if download_test.status == 200 else 'FAILED' }}"
          - "========================================================="
