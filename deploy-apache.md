# Installation d'un serveur Web Apache/PHP/MySQL

## Travail a faire

- Installation de Apache comme service Windows
- Installation de PHP
- Configuration de PHP comme module Apache
- Install https
  - OpenSSL 


## Critère de validation

- Installation de Apache comme serveur
- Déploiement du prototype

## Commandes 

```bash
Listen *:80
LoadModule rewrite_module modules/mod_rewrite.so
ServerName localhost:80
AllowOverride All
```

```bash
cd /Apache24/bin
httpd -t
```
install Apache as a Windows service

```bash
cd /Apache24/bin
httpd -k install
```

## Références 
- https://www.sitepoint.com/how-to-install-apache-on-windows/
- https://www.sitepoint.com/how-to-install-php-on-windows/#step5configurephpasanapachemodule