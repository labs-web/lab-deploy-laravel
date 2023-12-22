# Installation Https 

Commande openssl

```bash
openssl req -x509 -nodes -days 1095 -newkey rsa:2048 -out server.crt -keyout server.key
```
```bash
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^ https://%{SERVER_NAME}%{REQUEST_URI} [END,NE,R=permanent]
```