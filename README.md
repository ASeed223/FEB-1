Audience:
Configuration Management Team
After reading this you will be able to: 
Generate a public-private key and create a csr (certificate signing request) to get a certificate back.
Create a Keystore and/or truststore
Perform the steps neccessary for a server application to host using https
Pre-requisites:
AIX / Linux or Windows with Ming or Git installed with a bash shell. - You will be using openssl and keytool.
Best done in the office where you have access to the development team to help with merges.
Overview:
Benefits: openssl and keytool are on every Linux box and available using Git Bash.
Create private RSA key file:
             What is it?  RSA is a private key based on RSA Algorithm. This is used during SSL / TLS for symmetric key exchange and authentication. Within the private RSA key file is the public key

 Generate the RSA private key file on the host server, in the home directory. Here I made an /ssl directory to keep things organized. It is best to do these activities on a RHEL box, Windows implementation has restrictions.
 

openssl genrsa -aes256 -out <ServerAppName>.key 2048 ( or 4096) (This will output to screen)

Example: To create a secure key file, using AES256 encryption, which will require a passphrase, with key size of 4096, this need to be run on a linux server.

 openssl genrsa -aes256  -out <ServerappName>.key 4096

(The .key file is PEM based)

$ openssl genrsa -aes128 -out jenkins.key 2048

 The output will look similar to this:
Generating RSA private key, 2048 bit long modulus

....+++                                

...................................................................................+++

e is 65537 (0x10001)

Enter pass phrase for jenkins.key: ****************

Verifying - Enter pass phrase for jenkins.key: ****************

Check that the RSA key is ok.
 ​openssl rsa -check -in <ServerAppName>.key
The output will look like:

RSA key ok

writing RSA key

-----BEGIN RSA PRIVATE KEY-----

MIIEpAIBAAKCAQEAq4aue4bK/Am9OLBOGxL8PoLypTffoZPDd7Y8u2c6pwPaXSO+

//vh+5nUBujomTvFXaX7FeKnIULenC8lFkNItMiGFqKv6zQrl9lEM4oA==

-----END RSA PRIVATE KEY-----

 From the RSA private key file, generate a CSR, certificate signing request. (This is the same as IBM’s KeyManager .arm file. )
 Create a san.cnf file to provide information to the csr when it is created.
For example, replace values where appropriate
$ touch san.cnf
$ vi san.cnf

[ req ]
prompt = no
default_bits = 4096
distinguished_name = dn
req_extensions = req_ext
[ dn ]
C = US
ST = CA
L = Saramento
O = StateOfCalifornia
OU = FranchiseTaxBoard
CN = ftbjenkins
emailAddress = edrbuildmaster@ftb.ca.gov or FTBEDRCMTeam@ftb.ca.gov
[ req_ext ]
subjectAltName = @alt_names
[alt_names]
DNS.1 = ftbjenkins
DNS.2 = ftbjenkins.ftb.ca.gov
DNS.3 = lxpd191
DNS.4 = lxpd191.ftb.ca.gov
DNS.5 = edrbuildmaster
DNS.6 = edrbuildmaster.ftb.ca.gov
           Legend to the san.cnf file

          default_bits = this is the key size, 2048 or 4096   

           C — Country
           ST — State
           L — City
           O — Organization
          OU — Organization Unit
          CN — Common Name (eg: the main domain the certificate should cover)-

(The Common Name (CN) field is often misunderstood and is filled out incorrectly. Mine was kicked backed and I had to explain that it wasn't a bogus name.
The Common Name is typically composed of Host + Domain Name and will look like “ftbjenkins” or “yoursite.com”.)
emailAddress — main administrative point of contact for the certificate. _> FTBEDRCMTeam@ftb.ca.gov

After the san.cnf file is created use the template below to create the csr.
             openssl req -new -config san.cnf -key <ServerAppName>.key –out <ServerAppName>.csr

           $openssl req -new -config san.cnf -key jenkins.key -out jenkins.csr

After the csr is generated, the follow site is used by our CA (certificate authority) to check your csr.
https://redkestrel.co.uk/products/decoder/
Send csr using CA Service Center to WSMG for signing.

Convert DER formatted signed certificate into a readable PEM formatted certificate. (If neccessary)
The resulting .csr (CSR) file is sent to WSMG as a request to sign. WSMG then sends back a .cer (CER) file.
If the .cer file is in a DER format (.crt .cer .der) then it must be converted to a PEM file to be imported into a keystore. (You can name the output file whatever you want, so it's easy to remember what you have.)
          openssl x509 -in jenkins.cer -inform der -out signed_jenkins.pem

Now verify that the resulting PEM file is ok.
           openssl x509 -noout -modulus -in signed_jenkins.pem | openssl sha256

If the above command produced an error, see if you can open the .cer file in Notepad. if you can read it.
For example:
 -----BEGIN CERTIFICATE-----
bunch of lines of text
-----END CERTIFICATE-----
Then you do not need to convert it to a pem file. However check that the very top and last line say BEGIN CERTIFICATE and END CERTIFICATE. there should be no writting outside the lines.

Next. You need to place the signed cert in the same directory you used to make the:
   <server>.csr
   <server>.key
    san.cnf

Create a new keystore (you can give it the same name as the old one, if replacing. So you don't have to change the cmd string)
Using ftbnexus as an example, we create a .p12 file first using the signed cert and key.
openssl pkcs12 -export -in ftbnexus.cer -inkey ftbnexus.key -out ftbnexus.p12
Then use keytool to create a .jks , a keystore.
keytool -importkeystore -srckeystore ftbnexus.p12 -srcstoretype PKCS12 -destkeystore nexusrepo.jks -deststoretype JKS
You can now check it out, you will not see the signed cert just the key.
keytool -list -keystore nexusrepo.jks
Then you can import ftb-0 , Zscaler, or another server if needed.
keytool -importcert -file Zscaler.cer -keystore nexusrepo.jks -alias 'zscaler'
Now the keystore is ready to use.
