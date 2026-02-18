This guide focuses on setting up SSL for Apache (httpd) on servers like lxpd195 where automated service restarts are a must.

The Problem: Standard SSL keys often use encryption (like -aes256), which forces Apache to stop and ask for a password every time it starts up. If you aren't there to type it in, the service stays down (Error: AH01969: Requesting pass phrase).

The Fix: We use the -nodes (No DES) flag during generation. This creates an unencrypted private key, allowing Apache to read it instantly and boot up automatically without any manual intervention.
