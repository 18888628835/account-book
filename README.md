## front-end

yarn install

yarn build

## docker

docker compose up -d

## generate ssl

this project supports protocol `http2`,please run the following command

```
openssl genrsa -des3 -passout pass:x -out server.pass.key 2048

openssl rsa -passin pass:x -in server.pass.key -out server.key

openssl req -new -key server.key -out server.csr

openssl x509 -req -sha256 -days 3650 -in server.csr -signkey server.key -out server.crt
```
