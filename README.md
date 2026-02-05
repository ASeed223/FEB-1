    - name: "[lxpd208] Start new service (Attempt 1)"
      ansible.builtin.shell: "{{ nexus_link }}/bin/nexus start"

    - name: "[lxpd208] Health Check (Wait for HTTP 200)"
      ansible.builtin.uri:
        url: "https://lxpd208:8443/service/rest/v1/status"
        validate_certs: no
        status_code: 200
      register: health_208
      until: health_208.status == 200
      retries: 10
      delay: 10
      ignore_errors: yes
