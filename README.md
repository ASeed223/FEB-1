Step 2: Generate the Password-Less Key & CSR
This is the most critical step for Apache automation. We use the -nodes flag to ensure the private key is not encrypted.

Run this command inside /home/cmdeploy/2026Cert:
openssl req -new -newkey rsa:4096 -nodes \
  -keyout ftbnexus.key \
  -out ftbnexus.csr \
  -config san.cnf

  You now have two files:

ftbnexus.key: The Private Key (No password). Keep this safe on the server.

ftbnexus.csr: The Request File (Send this to WSMG).
