Create the config file (san.cnf):
Modern browsers require Subject Alternative Names (SANs).
[ req ]
prompt = no
default_bits = 4096
distinguished_name = dn
req_extensions = req_ext

[ dn ]
C = US
ST = CA
L = Sacramento
O = StateOfCalifornia
OU = FranchiseTaxBoard
CN = ftbnexus.ftb.ca.gov   # Main FQDN
emailAddress = FTBEDRCMTeam@ftb.ca.gov

[ req_ext ]
subjectAltName = @alt_names

[alt_names]
# Add all aliases here
DNS.1 = ftbnexus
DNS.2 = ftbnexus.ftb.ca.gov
DNS.3 = lxpd195
DNS.4 = lxpd195.ftb.ca.gov
