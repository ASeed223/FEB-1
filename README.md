openssl req -new -newkey rsa:4096 -nodes \
  -keyout ftbnexus.key \
  -out ftbnexus.csr \
  -config san.cnf
