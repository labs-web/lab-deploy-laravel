# Installation d'un serveur Web Apache/PHP/MySQL

## Travail a faire

- Installation de Apache comme service Windows
- Installation de PHP
- Configuration de PHP comme module Apache
- Install https
  - OpenSSL 


## Critère de validation

1. Déploiement de lab-laravel-crud-basic sans VirtuelHost
   - Fichier de configuration apache par défaut
   - Fichier de configuration apache
   - Référence
2. Déploiement de lab-laravel-crud-standard dans le même serveur 
   - Fichier de configuration apache
   - Référence
3. Installation de HTTPS sur lab-laravel-crud-basic
   - Commandes
   - Référence


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
- https://www.youtube.com/watch?v=cBa87N_BZ4s&ab_channel=BoostMyTool
- https://www.youtube.com/watch?v=7KHEmFJv4VE&ab_channel=tutortechie