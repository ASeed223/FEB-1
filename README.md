Step 4: Submit to WSMG (via FreshService)
Grab the CSR content:
Run the following command to print your request to the screen:


cat ftbnexus.csr
The FreshService Workaround: Gotcha: FreshService will block .csr file uploads. To get around this, copy the entire terminal output (making sure to include the -----BEGIN and -----END lines) and paste it into a local Notepad file. Save it as ftbnexus.csr.txt.

Open a Ticket:
Submit a General Service Request in FreshService, attach your ftbnexus.csr.txt file, and explicitly ask them to return the signed certificate in Base64/PEM format.
