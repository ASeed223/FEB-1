[root@lxpd195 ~]# journalctl -xeu httpd.service
-- Subject: Unit httpd.service has failed
-- Defined-By: systemd
-- Support: https://access.redhat.com/support
--
-- Unit httpd.service has failed.
--
-- The result is failed.
Jan 31 03:19:01 lxpd195 systemd[1]: httpd.service: Unit cannot be reloaded because it is inactive.
Feb 12 08:37:33 lxpd195 systemd[1]: Starting The Apache HTTP Server...
-- Subject: Unit httpd.service has begun start-up
-- Defined-By: systemd
-- Support: https://access.redhat.com/support
--
-- Unit httpd.service has begun starting up.
Feb 12 08:37:33 lxpd195 httpd[2196509]: [Thu Feb 12 08:37:33.731323 2026] [so:warn] [pid 2196509:tid 140044738289344] AH01574: module proxy_module is already loaded, skipping
Feb 12 08:37:33 lxpd195 httpd[2196509]: [Thu Feb 12 08:37:33.731518 2026] [so:warn] [pid 2196509:tid 140044738289344] AH01574: module proxy_http_module is already loaded, skipping
Feb 12 08:37:33 lxpd195 httpd[2196509]: [Thu Feb 12 08:37:33.731527 2026] [so:warn] [pid 2196509:tid 140044738289344] AH01574: module proxy_balancer_module is already loaded, skipping
Feb 12 08:37:33 lxpd195 httpd[2196509]: [Thu Feb 12 08:37:33.731536 2026] [so:warn] [pid 2196509:tid 140044738289344] AH01574: module lbmethod_byrequests_module is already loaded, skipping
Feb 12 08:37:33 lxpd195 httpd[2196509]: [Thu Feb 12 08:37:33.731546 2026] [so:warn] [pid 2196509:tid 140044738289344] AH01574: module ssl_module is already loaded, skipping
Feb 12 08:37:33 lxpd195 httpd[2196509]: [Thu Feb 12 08:37:33.731555 2026] [so:warn] [pid 2196509:tid 140044738289344] AH01574: module proxy_ajp_module is already loaded, skipping
Feb 12 08:38:13 lxpd195 systemd[1]: httpd.service: Main process exited, code=exited, status=1/FAILURE
Feb 12 08:38:13 lxpd195 systemd[1]: httpd.service: Failed with result 'exit-code'.
-- Subject: Unit failed
-- Defined-By: systemd
-- Support: https://access.redhat.com/support
--
-- The unit httpd.service has entered the 'failed' state with result 'exit-code'.
Feb 12 08:38:13 lxpd195 systemd[1]: Failed to start The Apache HTTP Server.
-- Subject: Unit httpd.service has failed
-- Defined-By: systemd
-- Support: https://access.redhat.com/support
--
-- Unit httpd.service has failed.
--
-- The result is failed.
Feb 12 08:43:25 lxpd195 systemd[1]: Starting The Apache HTTP Server...
-- Subject: Unit httpd.service has begun start-up
-- Defined-By: systemd
-- Support: https://access.redhat.com/support
--
-- Unit httpd.service has begun starting up.
Feb 12 08:43:25 lxpd195 httpd[2197010]: [Thu Feb 12 08:43:25.762545 2026] [so:warn] [pid 2197010:tid 139845925695168] AH01574: module proxy_module is already loaded, skipping
Feb 12 08:43:25 lxpd195 httpd[2197010]: [Thu Feb 12 08:43:25.762698 2026] [so:warn] [pid 2197010:tid 139845925695168] AH01574: module proxy_http_module is already loaded, skipping
Feb 12 08:43:25 lxpd195 httpd[2197010]: [Thu Feb 12 08:43:25.762708 2026] [so:warn] [pid 2197010:tid 139845925695168] AH01574: module proxy_balancer_module is already loaded, skipping
Feb 12 08:43:25 lxpd195 httpd[2197010]: [Thu Feb 12 08:43:25.762718 2026] [so:warn] [pid 2197010:tid 139845925695168] AH01574: module lbmethod_byrequests_module is already loaded, skipping
Feb 12 08:43:25 lxpd195 httpd[2197010]: [Thu Feb 12 08:43:25.762727 2026] [so:warn] [pid 2197010:tid 139845925695168] AH01574: module ssl_module is already loaded, skipping
Feb 12 08:43:25 lxpd195 httpd[2197010]: [Thu Feb 12 08:43:25.762735 2026] [so:warn] [pid 2197010:tid 139845925695168] AH01574: module proxy_ajp_module is already loaded, skipping
Feb 12 08:43:39 lxpd195 systemd[1]: httpd.service: Main process exited, code=exited, status=1/FAILURE
Feb 12 08:43:39 lxpd195 systemd[1]: httpd.service: Failed with result 'exit-code'.
-- Subject: Unit failed
-- Defined-By: systemd
-- Support: https://access.redhat.com/support
--
-- The unit httpd.service has entered the 'failed' state with result 'exit-code'.
Feb 12 08:43:39 lxpd195 systemd[1]: Failed to start The Apache HTTP Server.
-- Subject: Unit httpd.service has failed
-- Defined-By: systemd
-- Support: https://access.redhat.com/support
--
-- Unit httpd.service has failed.
--
-- The result is failed.
...skipping...
-- Subject: Unit httpd.service has failed
-- Defined-By: systemd
-- Support: https://access.redhat.com/support
--
-- Unit httpd.service has failed.
--
-- The result is failed.
Jan 31 03:19:01 lxpd195 systemd[1]: httpd.service: Unit cannot be reloaded because it is inactive.
Feb 12 08:37:33 lxpd195 systemd[1]: Starting The Apache HTTP Server...
-- Subject: Unit httpd.service has begun start-up
-- Defined-By: systemd
-- Support: https://access.redhat.com/support
--
-- Unit httpd.service has begun starting up.
Feb 12 08:37:33 lxpd195 httpd[2196509]: [Thu Feb 12 08:37:33.731323 2026] [so:warn] [pid 2196509:tid 140044738289344] AH01574: module proxy_module is already loaded, skipping
Feb 12 08:37:33 lxpd195 httpd[2196509]: [Thu Feb 12 08:37:33.731518 2026] [so:warn] [pid 2196509:tid 140044738289344] AH01574: module proxy_http_module is already loaded, skipping
Feb 12 08:37:33 lxpd195 httpd[2196509]: [Thu Feb 12 08:37:33.731527 2026] [so:warn] [pid 2196509:tid 140044738289344] AH01574: module proxy_balancer_module is already loaded, skipping
Feb 12 08:37:33 lxpd195 httpd[2196509]: [Thu Feb 12 08:37:33.731536 2026] [so:warn] [pid 2196509:tid 140044738289344] AH01574: module lbmethod_byrequests_module is already loaded, skipping
Feb 12 08:37:33 lxpd195 httpd[2196509]: [Thu Feb 12 08:37:33.731546 2026] [so:warn] [pid 2196509:tid 140044738289344] AH01574: module ssl_module is already loaded, skipping
Feb 12 08:37:33 lxpd195 httpd[2196509]: [Thu Feb 12 08:37:33.731555 2026] [so:warn] [pid 2196509:tid 140044738289344] AH01574: module proxy_ajp_module is already loaded, skipping
Feb 12 08:38:13 lxpd195 systemd[1]: httpd.service: Main process exited, code=exited, status=1/FAILURE
Feb 12 08:38:13 lxpd195 systemd[1]: httpd.service: Failed with result 'exit-code'.
-- Subject: Unit failed
-- Defined-By: systemd
-- Support: https://access.redhat.com/support
--
-- The unit httpd.service has entered the 'failed' state with result 'exit-code'.
Feb 12 08:38:13 lxpd195 systemd[1]: Failed to start The Apache HTTP Server.
-- Subject: Unit httpd.service has failed
-- Defined-By: systemd
-- Support: https://access.redhat.com/support
--
-- Unit httpd.service has failed.
--
-- The result is failed.
Feb 12 08:43:25 lxpd195 systemd[1]: Starting The Apache HTTP Server...
-- Subject: Unit httpd.service has begun start-up
-- Defined-By: systemd
-- Support: https://access.redhat.com/support
--
-- Unit httpd.service has begun starting up.
Feb 12 08:43:25 lxpd195 httpd[2197010]: [Thu Feb 12 08:43:25.762545 2026] [so:warn] [pid 2197010:tid 139845925695168] AH01574: module proxy_module is already loaded, skipping
Feb 12 08:43:25 lxpd195 httpd[2197010]: [Thu Feb 12 08:43:25.762698 2026] [so:warn] [pid 2197010:tid 139845925695168] AH01574: module proxy_http_module is already loaded, skipping
Feb 12 08:43:25 lxpd195 httpd[2197010]: [Thu Feb 12 08:43:25.762708 2026] [so:warn] [pid 2197010:tid 139845925695168] AH01574: module proxy_balancer_module is already loaded, skipping
Feb 12 08:43:25 lxpd195 httpd[2197010]: [Thu Feb 12 08:43:25.762718 2026] [so:warn] [pid 2197010:tid 139845925695168] AH01574: module lbmethod_byrequests_module is already loaded, skipping
Feb 12 08:43:25 lxpd195 httpd[2197010]: [Thu Feb 12 08:43:25.762727 2026] [so:warn] [pid 2197010:tid 139845925695168] AH01574: module ssl_module is already loaded, skipping
Feb 12 08:43:25 lxpd195 httpd[2197010]: [Thu Feb 12 08:43:25.762735 2026] [so:warn] [pid 2197010:tid 139845925695168] AH01574: module proxy_ajp_module is already loaded, skipping
Feb 12 08:43:39 lxpd195 systemd[1]: httpd.service: Main process exited, code=exited, status=1/FAILURE
Feb 12 08:43:39 lxpd195 systemd[1]: httpd.service: Failed with result 'exit-code'.
-- Subject: Unit failed
-- Defined-By: systemd
-- Support: https://access.redhat.com/support
--
-- The unit httpd.service has entered the 'failed' state with result 'exit-code'.
Feb 12 08:43:39 lxpd195 systemd[1]: Failed to start The Apache HTTP Server.
-- Subject: Unit httpd.service has failed
-- Defined-By: systemd
-- Support: https://access.redhat.com/support
--
-- Unit httpd.service has failed.
--
-- The result is failed.
