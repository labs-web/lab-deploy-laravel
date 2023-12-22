# Fichier de configuration apache

```bash
Listen *:80
LoadModule rewrite_module modules/mod_rewrite.so
<Directory "C:\Apache24\htdocs">
    Options Indexes FollowSymLinks
    AllowOverride All
    Require all granted
</Directory>
ServerName localhost:80
# PHP8 module
PHPIniDir "C:/php"
LoadModule php_module "C:/phpApache/php8apache2_4.dll"
AddType application/x-httpd-php .php
```

## Référence

- [configure php as an apache module](https://www.sitepoint.com/how-to-install-php-on-windows/#step5configurephpasanapachemodule)