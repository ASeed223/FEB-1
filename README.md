Nexus HA Reverse Proxy Setup
This is a concise Wiki guide for the Nexus HA Migration project. It documents the paths, configurations, and critical security settings we verified to get the 8443 proxy running.

New Virtual Host：/etc/httpd/conf.d/virtual_hosts.conf （Contains port 8443 (later 8444) listener, SSL settings, and Proxy balancer rules.）
Old SSL Config： /etc/httpd/conf.d/ssl.conf （Must be fully commented out to avoid port 8444 conflicts and old certificate errors.）
Main Config： /etc/httpd/conf/httpd.conf （Defines the global User and Group (set to apache).

2. Certificate & Log Paths
Since certificates are stored in a non-standard home directory, specific paths and labels are required.

SSL Certificate (.pem): /home/cmdeploy/2026Cert/ftbnexus.pem

SSL Private Key (.key): /home/cmdeploy/2026Cert/ftbnexus.key

Proxy Error Logs: /var/log/httpd/test_8443_error.log

Proxy Access Logs: /var/log/httpd/test_8443_access.log

3. Required Permissions & Security
Apache runs as the apache user. It requires "traversal" rights to reach the certificates and special labels to bypass SELinux.

Directory Permissions
Home Directory (/home/cmdeploy/): Must be 711 (drwx--x--x). This allows Apache to enter the directory without seeing other files.

Cert Directory (/home/cmdeploy/2026Cert/): Must be 755 (drwxr-xr-x).

File Permissions
Cert & Key Files: Minimum 644 (-rw-r--r--) for testing, or 640 with group ownership set to apache.

SELinux Context (Critical)
Because files are in /home/, they must have the cert_t security label to be readable by Apache:

Command: chcon -t cert_t /home/cmdeploy/2026Cert/ftbnexus.*

Verify: ls -lZ should show unconfined_u:object_r:cert_t:s0.

4. Key Apache Directives for HA Compatibility
To ensure the proxy connects successfully to the back-end Nexus nodes (10.240.240.207/208), these settings were required in virtual_hosts.conf:

SSLProxyEngine On: Enables SSL for the back-end connection.

SSLProxyCheckPeerName off: Disables hostname verification (required because back-end certs use nexus01/nexus02 instead of the load balancer name).

SSLProxyCheckPeerCN off: Disables Common Name verification.

SSLProxyVerify none: Skips back-end certificate chain validation.

5. Useful Operational Commands
Syntax Check: /usr/sbin/httpd -t

Check Logs: tail -f /var/log/httpd/test_8443_error.log (Requires ACL access)

Verify Listener: ss -tulpn | grep :8443
