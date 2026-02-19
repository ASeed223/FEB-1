Pre-work - 
On lxpd195:
Copy /etc/httpd/conf.d/ssl.conf from lxpd207 and modify lxpd195:/etc/httpd/conf.d/ssl.conf.
Implementation / Cut-over:
CM Team (devOps)
on lxpd195 the file is /etc/httpd/conf.d/virtual_hosts.conf, this is structured the same as lxpd207: /etc/httpd/conf.d/httpd.conf. This file has been modified already and will need to be copied over the existing virtual_hosts.conf before cut-over. 

The cutover begins after a last sync between Prod Nexus storage and database backup to Dev Nexus storage and database. And after the the HA systems have been restarted and the Blob storage path's have been validated.
As soon as the storage and dB syncs have completed. 
- Shut down Nexus on lxpd195. (Do not restart)
- Shut down Apache on lxpd195.
- Copy the contents of /home/cmdeploy/virtual_hosts.conf to /etc/httpd/conf.d/virtual_hosts.conf since root owns the file, we cannot copy or delete files in the conf.d directory.
-Shutdown Apache on lxpd207
-Start up Apache on lxpd195 , this will start serving the HA Nexus servers immediately. 
Rollback.
Shutdown Apache on lxpd195.
Startup Nexus on lxpd195.

