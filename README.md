Pre-work - On lxpd195:

Verify the 2026 SSL certificates are located in /home/cmdeploy/2026Cert/ with proper permissions and the SELinux cert_t label applied (Already validated during port 8443 testing).

Ensure /etc/httpd/conf.d/ssl.conf is fully commented out (especially the Listen 8444 directive and old certificate paths) to prevent port conflicts and SSL mismatch errors.

Prepare the final configuration content for virtual_hosts.conf (changing the tested proxy port from 8443 to 8444).

Implementation / Cut-over:
CM Team (devOps)
On lxpd195, the file /etc/httpd/conf.d/virtual_hosts.conf manages the reverse proxy and load balancing to the backend HA cluster (lxpd207 & lxpd208). This file has been tested successfully on port 8443 and will need to be updated to port 8444 before cut-over.

The cutover begins after a last sync between Prod Nexus storage and database backup to Dev Nexus storage and database. And after the HA systems have been restarted and the Blob storage paths have been validated.
As soon as the storage and dB syncs have completed:

Shut down the legacy Nexus service on lxpd195 (sudo systemctl stop nexus).

Disable the legacy Nexus service on lxpd195 to prevent auto-restart (sudo systemctl disable nexus).

Shut down Apache on lxpd207 (Retiring the old proxy entry point).

On lxpd195, update the proxy port: Change Listen 8443 to Listen 8444 and <VirtualHost *:8443> to <VirtualHost *:8444> in /etc/httpd/conf.d/virtual_hosts.conf. (Copy the contents from your staged file in /home/cmdeploy/ into /etc/httpd/conf.d/virtual_hosts.conf since root owns the destination file).

Verify Apache syntax on lxpd195 (/usr/sbin/httpd -t).

Start up / Restart Apache on lxpd195 (sudo systemctl restart httpd). This will bind to port 8444 and start serving the HA Nexus servers immediately.

Rollback:

Shutdown Apache on lxpd195 (sudo systemctl stop httpd).

Start up Apache on lxpd207 (Restore the previous HA proxy entry point).

Start up the legacy Nexus service on lxpd195 (sudo systemctl start nexus).
