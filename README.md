Step 3: Verify CSR Locally (Safety First)
Do not paste the CSR into online decoders. Verify it directly on the server to check if the SANs (aliases) are correct.


openssl req -text -noout -verify -in ftbnexus.csr


Check the output for X509v3 Subject Alternative Name and ensure lxpd195 and ftbnexus are listed.
