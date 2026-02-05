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

    - name: "[lxpd208] Final Health Check (HTTP 200)"
      ansible.builtin.uri:
        url: "https://lxpd208:8443/service/rest/v1/status"
        validate_certs: no
        status_code: 200
      register: health_208
      until: health_208.status == 200
      retries: 20
      delay: 10


      
TASK [[lxpd208] Start Service with Smart Retry] ********************************
fatal: [lxpd208]: FAILED! => {"msg": "The task includes an option with an undefi       ned variable. The error was: 'nexus_link' is undefined. 'nexus_link' is undefine       d\n\nThe error appears to be in '/opt/appdata/edrcmtools/working/gitrepos/temp/s       hushen/ansibleNexus/nexus/update_nexus.yaml': line 126, column 7, but may\nbe el       sewhere in the file depending on the exact syntax problem.\n\nThe offending line        appears to be:\n\n\n    - name: \"[lxpd208] Start Service with Smart Retry\"\n             ^ here\n"}
