Step 5: Install and Validate the New Certificate
Once the ticket is resolved, you should receive a certificate in PEM format. Transfer this file into the same directory where you generated the private key (/home/cmdeploy/2026Cert/) and ensure you validate your changes.

Move the file:
Upload the file (e.g., ftbnexus.cer) to /home/cmdeploy/2026Cert/.

Verify the match:
Run this command to ensure the new certificate and your private key actually match:
openssl x509 -noout -modulus -in ftbnexus.cer | openssl md5
openssl rsa -noout -modulus -in ftbnexus.key | openssl md5

Update Apache:
Update the SSLCertificateFile path in your Apache configuration to point to this new file.
