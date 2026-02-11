- name: Display Final Validation Summary
      ansible.builtin.debug:
        msg:
          - "========================================================="
          - "  NEXUS LXPD195 VALIDATION REPORT"
          - "========================================================="
          - "Target Host    : {{ inventory_hostname }}"
          - "HTTPS Port     : {{ 'UP' if not port_check.failed else 'DOWN' }} ({{ nexus_port }})"
          - "System Status  : {{ 'PASSED' if api_status.status == 200 else 'FAILED (' ~ api_status.status | default('No Response') ~ ')' }}"
          - "Storage Write  : {{ 'PASSED' if db_writable.status == 200 else 'FAILED' }}"
          - "Download Test  : {{ 'PASSED' if download_test.status == 200 else 'FAILED' }}"
          - "========================================================="
