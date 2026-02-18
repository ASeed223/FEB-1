
openssl req -new -newkey rsa:4096 -nodes \
  -keyout lxpd195.key \
  -out lxpd195.csr \
  -config san.cnf
