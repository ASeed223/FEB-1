---
- name: Nexus HA Full Automated Upgrade
  hosts: lxpd208
  gather_facts: no
  any_errors_fatal: true
  
  vars_prompt:
    - name: "target_version"
      prompt: "Enter target version (e.g. 3.87.1)"
      private: no

  vars:
    # -------------------------------------------------------
    # PATH & USER CONFIGURATION
    # -------------------------------------------------------
    nexus_root: "/opt/nexus"
    nexus_link: "/opt/nexus/nexus"
    nexus_data_dir: "/opt/nexus/sonatype-work/nexus3"
    nexus_ssl_dir: "/opt/nexus/ssl"
    
    # Ownership (Matched to your environment)
    deploy_user: "cmdeploy"
    deploy_group: "edrstaff"
    secondary_node: "lxpd209"

    # -------------------------------------------------------
    # PERFORMANCE & SSL CONFIGURATION
    # -------------------------------------------------------
    nexus_xms: "6G"
    nexus_xmx: "6G"
    nexus_max_direct_memory: "15530M"
    
    keystore_filename: "nexus01.jks"
    # Plain text password for JVM (nexus.vmoptions)
    keystore_password: "edrcmadm"
    
    # Encrypted OBF Password for Jetty (jetty-https.xml)
    keystore_password_obf: !vault |
          $ANSIBLE_VAULT;1.1;AES256
          61366338363366303634633763356166376432646562643066343466643532623532373030383266
          6137333635373734386662653735383330303034333838330a663164613933646361366461316265
          66613638306333316435306632363064626334356332316238383462346536396262363431386461
          6132336431653139630a333532306132616139643766353466636331653032613865333564336265
          38626533366138633132636332616564303764363862326138333838313666346631636666613138
          6636393738393032383330323963653232656132623966633939

  tasks:
    # =======================================================
    # PHASE 1: PREPARATION & EXTRACTION
    # =======================================================
    - name: "Find Nexus tarball on lxpd208"
      ansible.builtin.find:
        paths: "{{ nexus_root }}"
        patterns: "*{{ target_version }}*.tar.gz"
      register: nexus_tarballs

    - name: "Fail if tarball is missing"
      ansible.builtin.fail:
        msg: "No tarball found for version {{ target_version }}"
      when: nexus_tarballs.matched == 0

    - name: "Set version and path facts"
      ansible.builtin.set_fact:
        nexus_tarball: "{{ (nexus_tarballs.files | sort(attribute='mtime') | last).path }}"
        extracted_dir_name: "{{ (nexus_tarballs.files | sort(attribute='mtime') | last).path | basename | regex_replace('(-unix|-linux-x86_64)?\\.tar\\.gz$', '') }}"

    - name: "Define new directory path"
      ansible.builtin.set_fact:
        new_nexus_dir: "{{ nexus_root }}/{{ extracted_dir_name }}"

    - name: "Extract Nexus on lxpd208"
      ansible.builtin.unarchive:
        src: "{{ nexus_tarball }}"
        dest: "{{ nexus_root }}"
        remote_src: yes
        creates: "{{ new_nexus_dir }}"
        owner: "{{ deploy_user }}"
        group: "{{ deploy_group }}"

    # =======================================================
    # PHASE 2: CONFIGURATION (USING TEMPLATES)
    # =======================================================
    - name: "Deploy nexus.vmoptions to new version"
      ansible.builtin.template:
        src: templates/nexus.vmoptions.j2
        dest: "{{ new_nexus_dir }}/bin/nexus.vmoptions"
        owner: "{{ deploy_user }}"
        group: "{{ deploy_group }}"
        mode: '0644'

    - name: "Deploy jetty-https.xml to new version"
      ansible.builtin.template:
        src: templates/jetty-https.xml.j2
        dest: "{{ new_nexus_dir }}/etc/jetty/jetty-https.xml"
        owner: "{{ deploy_user }}"
        group: "{{ deploy_group }}"
        mode: '0644'

    - name: "Verify SSL Certificate exists (Safety Check)"
      ansible.builtin.stat:
        path: "{{ nexus_ssl_dir }}/{{ keystore_filename }}"
      register: cert_check
      failed_when: not cert_check.stat.exists

    # =======================================================
    # PHASE 3: SYNC TO SECONDARY NODE
    # =======================================================
    - name: "Sync configured folder to {{ secondary_node }} using rsync"
      ansible.builtin.shell: "rsync -avzP {{ new_nexus_dir }}/ {{ secondary_node }}:{{ new_nexus_dir }}/"
      register: rsync_result

    # =======================================================
    # PHASE 4: UPGRADE LXPD208 (PRIMARY)
    # =======================================================
    - name: "[lxpd208] Stop service"
      ansible.builtin.shell: "{{ nexus_link }}/bin/nexus stop"
      failed_when: false

    - name: "[lxpd208] Wait for process to exit"
      ansible.builtin.shell: ps -ef | grep java | grep "org.sonatype.nexus.bundle.Main" | grep -v grep
      register: wait_stop_208
      until: wait_stop_208.rc != 0
      retries: 12
      delay: 5
      failed_when: false

    - name: "[lxpd208] Update softlink to {{ target_version }}"
      ansible.builtin.file:
        src: "{{ new_nexus_dir }}"
        dest: "{{ nexus_link }}"
        state: link
        owner: "{{ deploy_user }}"
        group: "{{ deploy_group }}"
        force: yes

    - name: "[lxpd208] Start new service (Attempt 1)"
      ansible.builtin.shell: "{{ nexus_link }}/bin/nexus start"

    - name: "[lxpd208] Health Check (Wait for HTTP 200)"
      ansible.builtin.uri:
        url: "https://lxpd208:8443/service/rest/v1/status"
        validate_certs: no
        status_code: 200
      register: health_208
      until: health_208.status == 200
      retries: 30
      delay: 10
      ignore_errors: yes

    # Retry logic for Primary Node
    - name: "[lxpd208] Start new service (Attempt 2 - if failed)"
      ansible.builtin.shell: "{{ nexus_link }}/bin/nexus start"
      when: health_208 is failed

    - name: "[lxpd208] Health Check (Retry)"
      ansible.builtin.uri:
        url: "https://lxpd208:8443/service/rest/v1/status"
        validate_certs: no
        status_code: 200
      register: health_208_retry
      until: health_208_retry.status == 200
      retries: 30
      delay: 10
      when: health_208 is failed
      ignore_errors: yes

    # =======================================================
    # PHASE 5: UPGRADE LXPD209 (SECONDARY)
    # =======================================================
    - name: "[lxpd209] Stop service"
      ansible.builtin.shell: "{{ nexus_link }}/bin/nexus stop"
      delegate_to: "{{ secondary_node }}"
      failed_when: false

    - name: "[lxpd209] Wait for process to exit"
      ansible.builtin.shell: ps -ef | grep java | grep "org.sonatype.nexus.bundle.Main" | grep -v grep
      delegate_to: "{{ secondary_node }}"
      register: wait_stop_209
      until: wait_stop_209.rc != 0
      retries: 12
      delay: 5
      failed_when: false

    - name: "[lxpd209] Update softlink to {{ target_version }}"
      ansible.builtin.file:
        src: "{{ new_nexus_dir }}"
        dest: "{{ nexus_link }}"
        state: link
        owner: "{{ deploy_user }}"
        group: "{{ deploy_group }}"
        force: yes
      delegate_to: "{{ secondary_node }}"

    - name: "[lxpd209] Start new service"
      ansible.builtin.shell: "{{ nexus_link }}/bin/nexus start"
      delegate_to: "{{ secondary_node }}"

    - name: "[lxpd209] Health Check (Wait for HTTP 200)"
      ansible.builtin.uri:
        url: "https://{{ secondary_node }}:8443/service/rest/v1/status"
        validate_certs: no
        status_code: 200
      register: health_209
      until: health_209.status == 200
      retries: 30
      delay: 10
      ignore_errors: yes

    # =======================================================
    # PHASE 6: CLEANUP & SUMMARY
    # =======================================================
    - name: "Move tarball to archive folder on lxpd208"
      ansible.builtin.command: "mv {{ nexus_tarball }} {{ nexus_root }}/archive/"
      args:
        removes: "{{ nexus_tarball }}"

    - name: "Final Summary"
      ansible.builtin.debug:
        msg: 
          - "Upgrade to {{ target_version }} completed successfully."
          - "Primary (lxpd208) status: {{ health_208_retry.status | default(health_208.status) | default('Failed') }}"
          - "Secondary (lxpd209) status: {{ health_209.status | default('Failed') }}"
