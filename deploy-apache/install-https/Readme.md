# Installation Https 

## Travail à faire 
Installation de HTTPs avec openssl

## Téléchargement de openssl

## Installation de openssl

## Création des fichiers server.crt et server.key

1.Exécution de la commande suivant dans le répertoire

```
C:\Apache24\bin
```

```bash
openssl req -x509 -nodes -days 1095 -newkey rsa:2048 -out server.crt -keyout server.key
```

2.Copier les deux fichiers dans 

```
C:\Apache24\conf
```

3. Configuration de apache

configuration d'apache : httpd.conf

```conf
LoadModule ssl_module modules/mod_ssl.so
Include conf/extra/httpd-ssl.conf
```

```bash
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^ https://%{SERVER_NAME}%{REQUEST_URI} [END,NE,R=permanent]
```


4.configuration d'apache : httpd-ssl.conf


```conf
ServerName localhost:443
```


## Références 
- [How to Install OpenSSL on Windows](https://www.youtube.com/watch?v=cBa87N_BZ4s&ab_channel=BoostMyTool)
- [How to configure https and SSL certificate in apache server](https://www.youtube.com/watch?v=7KHEmFJv4VE&ab_channel=tutortechie)