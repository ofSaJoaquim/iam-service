# iam-service
Iam service with keycloak using docker-composer 

It's alterady to run. 
Put the https keys in https_key with same name of exemple or change in docker-compose.yml.
You can generate localhost key using the script:
openssl req -x509 -out crt.pem -keyout key.pem \
  -newkey rsa:2048 -nodes -sha256 \
  -subj '/CN=localhost' -extensions EXT -config <( \
   printf "[dn]\nCN=localhost\n[req]\ndistinguished_name = dn\n[EXT]\nsubjectAltName=DNS:localhost\nkeyUsage=digitalSignature\nextendedKeyUsage=serverAuth")
