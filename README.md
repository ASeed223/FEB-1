Listen 8443

#LoadModule proxy_module modules/mod_proxy.so
#LoadModule proxy_http_module modules/mod_proxy_http.so
#LoadModule proxy_balancer_module modules/mod_proxy_balancer.so
#LoadModule lbmethod_byrequests_module modules/mod_lbmethod_byrequests.so
#LoadModule ssl_module modules/mod_ssl.so
#LoadModule proxy_ajp_module  modules/mod_proxy_ajp.so
#LoadModule headers_module modules/mod_headers.so

SSLSessionCache         shmcb:/run/httpd/sslcache(512000)
SSLSessionCacheTimeout  300
SSLCipherSuite PROFILE=SYSTEM
SSLProxyCipherSuite PROFILE=SYSTEM

<VirtualHost 10.240.243.216:8443>
        ServerName ftbnexus.ftb.ca.gov
        ServerAlias ftbnexus
        
        <Directory "/var/www/html">
            Require all denied
        </Directory>
        
        SSLEngine on
        SSLProxyEngine on
        SSLCertificateFile "/home/cmdeploy/2026Cert/ftbnexus.pem"
        SSLCertificateKeyFile "/home/cmdeploy/2026Cert/ftbnexus.key"
        SSLProxyCACertificateFile  "/etc/pki/ca-trust/extracted/pem/tls-ca-bundle.pem"
        SSLCACertificateFile "/etc/pki/ca-trust/extracted/pem/tls-ca-bundle.pem"
        SSLProtocol All -SSLv2 -SSLv3

        ProxyPreserveHost On
        RequestHeader set X-Forwarded-Proto "https"
        RequestHeader set X-Forwarded-Port "8443"

        Header add Set-Cookie "ROUTEID=.%{BALANCER_WORKER_ROUTE}e; path=/" env=BALANCER_ROUTE_CHANGED

        <Proxy balancer://mycluster>
            BalancerMember https://nexus01.ftb.ca.gov:8443 route=node1
            BalancerMember https://nexus02.ftb.ca.gov:8443 route=node2
            ProxySet lbmethod=byrequests
            ProxySet stickysession=ROUTEID
        </Proxy>

        ProxyTimeout 600

        ProxyPass / balancer://mycluster/
        ProxyPassReverse / balancer://mycluster/

        LogLevel ssl:debug
        ErrorLog /home/cmdeploy/logs/test_8443_error.log
        CustomLog /home/cmdeploy/logs/test_8443_access.log combined

</VirtualHost>
