# SSL-apache

## Travail à faire 

Déploiement page web au server local apache avec ssl https

## Critére de validation

- Use apache server
- Install ssl au server apache

## Commande

```bash

# Configuration file httpd.conf sur Appache24\conf

LoadModule ssl_module modules/mod_ssl.so
LoadModule rewrite_module modules/mod_rewrite.so
LoadModule socache_shmcb_module modules/mod_socache_shmcb.so

<IfModule ssl_module>
SSLRandomSeed startup builtin
SSLRandomSeed connect builtin
</IfModule>

<VirtualHost 192.168.2.25:80>
    ServerName localhost:80
    DocumentRoot "C:\Apache24\htdocs\app"
    <Directory "C:\Apache24\htdocs\app">
        Options FollowSymLinks
        AllowOverride All
        Require all granted
        DirectoryIndex index.php
    </Directory>
</VirtualHost>


LoadModule php_module "C:\php-8.1.24\php8apache2_4.dll"
AddType application/x-httpd-php .php
PHPIniDir "C:\php-8.1.24"

```

```bash

# Configuration host on windows sur C:\Windows\System32\drivers\etc

192.168.2.25       localhost


```

```bash

# Configuration ssl key and crt

cd C:\\Apache24\bin

openssl req -new -out mysite.csr -keyout mysite.pem

openssl rsa -in mysite.pem -out mysite.key

```

```bash

# Configuration httpd-ssl.conf sur Apache24\conf\extra

ServerName 192.168.2.25:443

```