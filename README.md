-Xms{{ nexus_xms | default('2703m') }}
-Xmx{{ nexus_xmx | default('2703m') }}
-XX:MaxDirectMemorySize={{ nexus_max_direct_memory | default('2G') }}
-XX:+UnlockDiagnosticVMOptions
-XX:+LogVMOutput
-XX:LogFile={{ nexus_data_dir }}/log/jvm.log
-XX:-OmitStackTraceInFastThrow
-Djava.net.preferIPv4Stack=true
-Dfile.encoding=UTF-8

# SSL Settings (Injecting your custom SSL config)
-Djavax.net.ssl.trustStore={{ nexus_data_dir }}/etc/ssl/{{ keystore_filename }}
-Djavax.net.ssl.trustStorePassword={{ keystore_password }}
-Djavax.net.ssl.keyStore={{ nexus_data_dir }}/etc/ssl/{{ keystore_filename }}
-Djavax.net.ssl.keyStorePassword={{ keystore_password }}

# Path Settings (Replacing relative paths with absolute variable)
-Dkaraf.home=.
-Dkaraf.base=.
-Djava.util.logging.config.file=etc/spring/java.util.logging.properties
-Dkaraf.data={{ nexus_data_dir }}
-Dkaraf.log={{ nexus_data_dir }}/log
-Djava.io.tmpdir={{ nexus_data_dir }}/tmp
-Djdk.tls.ephemeralDHKeySize=2048

#
# additional vmoptions needed for Java9+
#
--add-reads=java.xml=java.logging
--add-opens
java.base/java.security=ALL-UNNAMED
--add-opens
java.base/java.net=ALL-UNNAMED
--add-opens
java.base/java.lang=ALL-UNNAMED
--add-opens
java.base/java.util=ALL-UNNAMED
--add-opens
java.naming/javax.naming.spi=ALL-UNNAMED
--add-opens
java.rmi/sun.rmi.transport.tcp=ALL-UNNAMED
--add-exports=java.base/sun.net.www.protocol.http=ALL-UNNAMED
--add-exports=java.base/sun.net.www.protocol.https=ALL-UNNAMED
--add-exports=java.base/sun.net.www.protocol.jar=ALL-UNNAMED
--add-exports=jdk.xml.dom/org.w3c.dom.html=ALL-UNNAMED
--add-exports=jdk.naming.rmi/com.sun.jndi.url.rmi=ALL-UNNAMED
--add-exports=java.security.sasl/com.sun.security.sasl=ALL-UNNAMED
--add-exports=java.base/sun.security.x509=ALL-UNNAMED
--add-exports=java.base/sun.security.rsa=ALL-UNNAMED
--add-exports=java.base/sun.security.pkcs=ALL-UNNAMED
