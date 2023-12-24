# Fichier de configuration apache

```bash
DocumentRoot "C:\CNMH-Centre-management\Branche technique\Labs\lab-crud-standard/public"
<Directory "C:\CNMH-Centre-management\Branche technique\Labs\lab-crud-standard/public">
    Options Indexes FollowSymLinks
    AllowOverride All
    Require all granted
</Directory>


```

## Référence

- [configure php as an apache module](https://www.sitepoint.com/how-to-install-php-on-windows/#step5configurephpasanapachemodule)
- [how-to-install-apache-on-windows](https://www.sitepoint.com/how-to-install-apache-on-windows/)