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
    nexus_root: "/opt/nexus"
    nexus_link: "/opt/nexus/nexus"
    nexus_data_dir: "/opt/nexus/sonatype-work/nexus3"
    nexus_ssl_dir: "/opt/nexus/ssl"
    deploy_user: "cmdeploy"
    deploy_group: "edrstaff"
    secondary_node: "lxpd209"
    nexus_xms: "6G"
    nexus_xmx: "6G"
    nexus_max_direct_memory: "15530M"
    keystore_filename: "nexus01.jks"
    # cmdeploy ansible vault --> KeePass
    # Encrypted keystore_password Password for vmoptions
    keystore_password: !vault |
          $ANSIBLE_VAULT;1.1;AES256
          30616539643930393839366339623336636331653339313665633738316666633163343537643438
          6631356565393961666162656236623437396331646264360a616238316466393137616639303135
          61396165343037383938386638623638633334323430663665353931313362663363616565646661
          6531613930653032320a636337383236363330663935613337323061393530393065653330663266
          3232

    # Encrypted OBF Password for Jetty (jetty-https.xml)
    keystore_password_obf: !vault |
          $ANSIBLE_VAULT;1.1;AES256
          32663739393236336536346133376361663036656335373436336338356264323461386536343533
          6534616338313532383836313235393865306464383366300a336663366437623537666364333163
          61643261386236613561626635373063663136303133656436353930633337303335613538623163
          3633666634663361380a636133663834643664333135646163663734653834353039356538643539
          32653430626337343936373537633664323036636534396131613231663530623239333732393237
          6335376263333037663665373137616334623938376437653835

  tasks:
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

    # PHASE 2: CONFIGURATION (USING TEMPLATES)
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

    # PHASE 3: SYNC TO SECONDARY NODE
    - name: "Sync configured folder to {{ secondary_node }} using rsync"
      ansible.builtin.shell: "rsync -avzP {{ new_nexus_dir }}/ {{ secondary_node }}:{{ new_nexus_dir }}/"
      register: rsync_result

    # PHASE 4: UPGRADE LXPD208 (PRIMARY)
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

    - name: "[lxpd208] Start Service with Smart Retry"
      ansible.builtin.shell: |
        echo "Attempting to start Nexus on lxpd208..."
        # 1. Force cleanup: try stopping first to avoid leftover lock files
        {{ nexus_link }}/bin/nexus stop || true
        sleep 5

        # 2. Start the service
        {{ nexus_link }}/bin/nexus start

        # 3. Poll port 8443 (max wait: 120 seconds)
        # Exit immediately with 0 once the port is open
        for i in {1..24}; do
          if timeout 1 bash -c 'cat < /dev/null > /dev/tcp/127.0.0.1/8443'; then
            echo "Port 8443 is OPEN. Success."
            exit 0
          fi
          sleep 5
        done

        # If port is still not open, exit 1 to trigger Ansible retry
        echo "Timeout: Port 8443 did not open."
        exit 1
      register: start_208_result
      until: start_208_result.rc == 0
      retries: 5       # Retry the entire task (including stop) up to 5 times
      delay: 10        # Wait 10 seconds between retries
      ignore_errors: yes

    - name: "[lxpd208] Final Health Check (HTTP 200)"
      ansible.builtin.uri:
        url: "https://lxpd208:8443/service/rest/v1/status"
        validate_certs: no
        status_code: 200
      register: health_208
      until: health_208.status == 200
      retries: 20
      delay: 10
      ignore_errors: yes

    # PHASE 5: UPGRADE LXPD209 (SECONDARY)
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

    # PHASE 6: CLEANUP & SUMMARY
    - name: "Move tarball to archive folder on lxpd208"
      ansible.builtin.command: "mv {{ nexus_tarball }} {{ nexus_root }}/archive/"
      args:
        removes: "{{ nexus_tarball }}"

    - name: "Final Summary"
      ansible.builtin.debug:
        msg: 
          - "Upgrade to {{ target_version }} completed successfully."
          - "Primary (lxpd208) status: {{ health_208.status | default('Failed') }}"
          - "Secondary (lxpd209) status: {{ health_209.status | default('Failed') }}"
