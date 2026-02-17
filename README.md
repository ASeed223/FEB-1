curl -u "admin:<ADMIN_PASSWORD>" \
  -X PUT "<NEXUS_URL>/service/rest/v1/secrets/encryption/re-encrypt" \
  -H "accept: application/json" \
  -H "Content-Type: application/json" \
  -d '{
    "secretKeyId": "encryption_key"
  }'
