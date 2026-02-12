[Thu Feb 12 08:37:33.736916 2026] [core:notice] [pid 2196509:tid 140044738289344] SELinux policy enabled; httpd running as context system_u:system_r:httpd_t:s0
[Thu Feb 12 08:37:33.740882 2026] [suexec:notice] [pid 2196509:tid 140044738289344] AH01232: suEXEC mechanism enabled (wrapper: /usr/sbin/suexec)
[Thu Feb 12 08:37:33.740975 2026] [ssl:info] [pid 2196509:tid 140044738289344] AH01914: Configuring server ftbnexus:8444 for SSL protocol
[Thu Feb 12 08:37:33.758099 2026] [ssl:debug] [pid 2196509:tid 140044738289344] ssl_engine_init.c(1311): AH01904: Configuring server certificate chain (0 CA certificates)
[Thu Feb 12 08:37:33.758151 2026] [ssl:debug] [pid 2196509:tid 140044738289344] ssl_engine_init.c(627): AH01893: Configuring TLS extension handling
[Thu Feb 12 08:37:33.759097 2026] [ssl:info] [pid 2196509:tid 140044738289344] AH02576: Attempting to load encrypted (?) private key ftbnexus:8444:0
[Thu Feb 12 08:37:33.759158 2026] [ssl:info] [pid 2196509:tid 140044738289344] AH01969: Init: Requesting pass phrase from dialog filter program (/usr/libexec/httpd-ssl-pass-dialog)
[Thu Feb 12 08:38:13.627477 2026] [ssl:emerg] [pid 2196509:tid 140044738289344] AH02580: Init: Pass phrase incorrect for key ftbnexus:8444:0
[Thu Feb 12 08:38:13.627533 2026] [ssl:emerg] [pid 2196509:tid 140044738289344] SSL Library Error: error:0D0680A8:asn1 encoding routines:asn1_check_tlen:wrong tag
[Thu Feb 12 08:38:13.627550 2026] [ssl:emerg] [pid 2196509:tid 140044738289344] SSL Library Error: error:0D08303A:asn1 encoding routines:asn1_template_noexp_d2i:nested asn1 error
[Thu Feb 12 08:38:13.627559 2026] [ssl:emerg] [pid 2196509:tid 140044738289344] SSL Library Error: error:0D0680A8:asn1 encoding routines:asn1_check_tlen:wrong tag
[Thu Feb 12 08:38:13.627570 2026] [ssl:emerg] [pid 2196509:tid 140044738289344] SSL Library Error: error:0D07803A:asn1 encoding routines:asn1_item_embed_d2i:nested asn1 error (Type=RSAPrivateKey)
[Thu Feb 12 08:38:13.627585 2026] [ssl:emerg] [pid 2196509:tid 140044738289344] SSL Library Error: error:04093004:rsa routines:old_rsa_priv_decode:RSA lib
[Thu Feb 12 08:38:13.627594 2026] [ssl:emerg] [pid 2196509:tid 140044738289344] SSL Library Error: error:0D0680A8:asn1 encoding routines:asn1_check_tlen:wrong tag
[Thu Feb 12 08:38:13.627604 2026] [ssl:emerg] [pid 2196509:tid 140044738289344] SSL Library Error: error:0D07803A:asn1 encoding routines:asn1_item_embed_d2i:nested asn1 error (Type=PKCS8_PRIV_KEY_INFO)
[Thu Feb 12 08:38:13.627612 2026] [ssl:emerg] [pid 2196509:tid 140044738289344] AH02312: Fatal error initialising mod_ssl, exiting.
[Thu Feb 12 08:38:13.627621 2026] [ssl:emerg] [pid 2196509:tid 140044738289344] AH02564: Failed to configure encrypted (?) private key ftbnexus:8444:0, check /etc/httpd/conf.d/ftbnexus.key
AH00016: Configuration Failed
[Thu Feb 12 08:43:25.766941 2026] [core:notice] [pid 2197010:tid 139845925695168] SELinux policy enabled; httpd running as context system_u:system_r:httpd_t:s0
[Thu Feb 12 08:43:25.767893 2026] [suexec:notice] [pid 2197010:tid 139845925695168] AH01232: suEXEC mechanism enabled (wrapper: /usr/sbin/suexec)
[Thu Feb 12 08:43:25.767965 2026] [ssl:info] [pid 2197010:tid 139845925695168] AH01914: Configuring server ftbnexus:8444 for SSL protocol
[Thu Feb 12 08:43:25.783616 2026] [ssl:debug] [pid 2197010:tid 139845925695168] ssl_engine_init.c(1311): AH01904: Configuring server certificate chain (0 CA certificates)
[Thu Feb 12 08:43:25.783680 2026] [ssl:debug] [pid 2197010:tid 139845925695168] ssl_engine_init.c(627): AH01893: Configuring TLS extension handling
[Thu Feb 12 08:43:25.783878 2026] [ssl:info] [pid 2197010:tid 139845925695168] AH02576: Attempting to load encrypted (?) private key ftbnexus:8444:0
[Thu Feb 12 08:43:25.783925 2026] [ssl:info] [pid 2197010:tid 139845925695168] AH01969: Init: Requesting pass phrase from dialog filter program (/usr/libexec/httpd-ssl-pass-dialog)
[Thu Feb 12 08:43:39.268104 2026] [ssl:debug] [pid 2197010:tid 139845925695168] ssl_engine_pphrase.c(333): AH02583: encrypted ftbnexus:8444:0 private key - pass phrase requested
[Thu Feb 12 08:43:39.268275 2026] [ssl:debug] [pid 2197010:tid 139845925695168] ssl_util_ssl.c(444): AH02412: [ftbnexus:8444] Cert matches for name 'ftbnexus' [subject: emailAddress=FTBEDRCMTeam@ftb.ca.gov,CN=ftbnexus,OU=FranchiseTaxBoard,O=StateOfCalifornia,L=Saramento,ST=CA,C=US / issuer: CN=ftb-2,DC=ftb,DC=ca,DC=gov / serial: 170005E2C8685D20961EC8DAAF00020005E2C8 / notbefore: Jul 11 22:00:46 2022 GMT / notafter: May 25 16:46:26 2027 GMT]
[Thu Feb 12 08:43:39.268297 2026] [ssl:info] [pid 2197010:tid 139845925695168] AH02568: Certificate and private key ftbnexus:8444:0 configured from /etc/httpd/conf.d/ftbnexus.pem and /etc/httpd/conf.d/ftbnexus.key
AH00016: Configuration Failed
