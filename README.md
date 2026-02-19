# 1. 检查证书文件的完整路径权限（查看 Apache 是否能一路“走”进文件夹）
namei -om /home/cmdeploy/2026Cert/ftbnexus.key

# 2. 检查具体的证书和私钥权限
ls -l /home/cmdeploy/2026Cert/ftbnexus.pem /home/cmdeploy/2026Cert/ftbnexus.key

# 3. 检查日志目录的权限（确认 Apache 有地方写日志）
ls -ld /var/log/httpd/

# 4. 检查配置文件本身的权限
ls -l /etc/httpd/conf.d/virtual_hosts.conf /etc/httpd/conf.d/ssl.conf

# 5. 检查系统安全策略（SELinux）状态
getenforce

# 6. 检查 Apache 到底是以哪个用户运行的
grep -E '^User|^Group' /etc/httpd/conf/httpd.conf
