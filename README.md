ls -lZ /home/cmdeploy/2026Cert/ftbnexus.*
[cmdeploy@lxpd195 ~]$ ls -lZ /home/cmdeploy/2026Cert/ftbnexus.*
-rw-r--r--. 1 cmdeploy edrcmadm unconfined_u:object_r:cert_t:s0 1939 Feb 18 14:21 /home/cmdeploy/2026Cert/ftbnexus.csr
-rw-r--r--. 1 cmdeploy edrcmadm unconfined_u:object_r:cert_t:s0 3276 Feb 18 14:21 /home/cmdeploy/2026Cert/ftbnexus.key
-rw-r--r--. 1 cmdeploy edrcmadm unconfined_u:object_r:cert_t:s0 5101 Feb 19 10:50 /home/cmdeploy/2026Cert/ftbnexus.pem


namei -om /home/cmdeploy/2026Cert/ftbnexus.key
[cmdeploy@lxpd195 ~]$ namei -om /home/cmdeploy/2026Cert/ftbnexus.key
f: /home/cmdeploy/2026Cert/ftbnexus.key
 dr-xr-xr-x root     root     /
 drwxr-xr-x root     root     home
 drwx--x--x cmdeploy edrcmadm cmdeploy
 drwxr-xr-x cmdeploy edrcmadm 2026Cert
 -rw-r--r-- cmdeploy edrcmadm ftbnexus.key


/usr/sbin/httpd -t
[cmdeploy@lxpd195 ~]$ /usr/sbin/httpd -t
Syntax OK
