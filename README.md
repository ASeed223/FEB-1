SSLProxyEngine On
    
    # 关闭对后端证书名字和域名的严格校验
    SSLProxyCheckPeerName off
    SSLProxyCheckPeerCN off
    # 可选：顺便关闭对后端证书是否过期的校验，防止将来后端证书忘了续期导致掉线
    SSLProxyCheckPeerExpire off
