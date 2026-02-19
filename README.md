
#load mods
LoadModule proxy_module modules/mod_proxy.so
LoadModule proxy_http_module modules/mod_proxy_http.so
LoadModule proxy_balancer_module modules/mod_proxy_balancer.so
LoadModule lbmethod_byrequests_module modules/mod_lbmethod_byrequests.so
LoadModule ssl_module modules/mod_ssl.so
LoadModule proxy_ajp_module  modules/mod_proxy_ajp.so

<VirtualHost 10.240.243.216:8444>
## /etc/httpd/conf.d
        ServerName https://ftbnexus:8444/
        ServerAlias ftbnexus.ftb.ca.gov
        <Directory "/var/www/html">
            Require all denied
        </Directory>



        # SSL Configuration

        SSLEngine on
        SSLProxyEngine on
        SSLCertificateFile "/etc/httpd/conf.d/ftbnexus.pem"
        SSLCertificateKeyFile "/etc/httpd/conf.d/ftbnexus.key"
        SSLProxyCACertificateFile  "/etc/pki/ca-trust/extracted/pem/tls-ca-bundle.pem"
        SSLCertificateChainFile "/etc/httpd/conf.d/ftbnexus.pem"
        SSLCACertificateFile "/etc/pki/ca-trust/extracted/pem/tls-ca-bundle.pem"
        SSLProtocol All -SSLv2 -SSLv3


        <Proxy balancer://mycluster>
        # backend servers
        BalancerMember https://nexus01.ftb.ca.gov:8443 route=node1
        BalancerMember https://nexus02.ftb.ca.gov:8443 route=node2
        ProxySet lbmethod=byrequests
        ProxyAddHeaders off
        ProxyPreserveHost off
        #ProxySet stickysession=ROUTEID
        </Proxy>

        ProxyPass / balancer://mycluster/
        ProxyPassReverse / balancer://mycluster/

        # other SSL Settings

        # Logging
        LogLevel ssl:debug
        #ErrorLog /home/cmdeploy/logs/loadbalancer_error.log
        #CustomLog /home/cmdeploy/logs/loadbalancer_access.log combined


</VirtualHost>

