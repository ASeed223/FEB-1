chmod 711 /home/cmdeploy

# 允许进入证书子文件夹
chmod 755 /home/cmdeploy/2026Cert

# 允许读取证书和私钥
chmod 644 /home/cmdeploy/2026Cert/ftbnexus.pem
chmod 644 /home/cmdeploy/2026Cert/ftbnexus.key

chcon -t cert_t /home/cmdeploy/2026Cert/ftbnexus.*
