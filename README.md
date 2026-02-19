# 1. 检查证书文件的完整路径权限（查看 Apache 是否能一路“走”进文件夹）
namei -om /home/cmdeploy/2026Cert/ftbnexus.key


[cmdeploy@lxpd195 ~]$ namei -om /home/cmdeploy/2026Cert/ftbnexus.key
f: /home/cmdeploy/2026Cert/ftbnexus.key
 dr-xr-xr-x root     root     /
 drwxr-xr-x root     root     home
 drwx------ cmdeploy edrcmadm cmdeploy
 drwxr-x--- cmdeploy edrcmadm 2026Cert
 -rw-r--r-- cmdeploy edrcmadm ftbnexus.key


# 2. 检查具体的证书和私钥权限
ls -l /home/cmdeploy/2026Cert/ftbnexus.pem /home/cmdeploy/2026Cert/ftbnexus.key

-rw-r--r--. 1 cmdeploy edrcmadm 3276 Feb 18 14:21 /home/cmdeploy/2026Cert/ftbnexus.key
-rw-r--r--. 1 cmdeploy edrcmadm 5101 Feb 19 10:50 /home/cmdeploy/2026Cert/ftbnexus.pem


# 3. 检查日志目录的权限（确认 Apache 有地方写日志）
ls -ld /var/log/httpd/
drwx------. 2 root root 4096 Feb 19 13:30 /var/log/httpd/

# 4. 检查配置文件本身的权限
ls -l /etc/httpd/conf.d/virtual_hosts.conf /etc/httpd/conf.d/ssl.conf


-rw-rw-rw-. 1 root     root     9192 Feb 19 13:21 /etc/httpd/conf.d/ssl.conf
-rwxrwxrwx. 1 cmdeploy edrcmadm 1949 Feb 19 13:33 /etc/httpd/conf.d/virtual_hosts.conf

# 5. 检查系统安全策略（SELinux）状态
getenforce


[cmdeploy@lxpd195 ~]$ getenforce
Enforcing

# 6. 检查 Apache 到底是以哪个用户运行的
grep -E '^User|^Group' /etc/httpd/conf/httpd.conf

[cmdeploy@lxpd195 ~]$ grep -E '^User|^Group' /etc/httpd/conf/httpd.conf
User apache
Group apache

