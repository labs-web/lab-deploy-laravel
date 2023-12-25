# Déploiement de lab-crud-laravel-basic

## Tâches à Réaliser

1. Installer Apache en tant que service Windows.
2. Installer PHP.
3. Configurer PHP en tant que module Apache.
4. Déployer lab-laravel-crud-basic.

## Critères de Validation

1. Déploiement de lab-laravel-crud-basic sans VirtualHost.
   - Fichier de configuration Apache par défaut.
   - Fichier de configuration Apache modifié.
   - Référence.

### Installer Apache en tant que service Windows

```bash
# Accéder au répertoire bin d'Apache
cd /Apache24/bin

# Exécuter la commande suivante pour tester la configuration d'Apache
httpd -t

# Installer Apache en tant que service Windows
httpd -k install
```

### Installer PHP

Vous pouvez installer PHP séparément d'Apache. Téléchargez l'installateur PHP pour Windows depuis le site officiel de PHP (https://windows.php.net/download/) et suivez l'assistant d'installation.

### Configuration de PHP en tant que module Apache

Après avoir installé PHP, vous devez le configurer en tant que module pour Apache. Ouvrez le fichier de configuration d'Apache (`httpd.conf`) et ajoutez les lignes suivantes :

```apache
# Définir le gestionnaire pour les fichiers PHP
AddHandler application/x-httpd-php .php

# Définir le type MIME pour les fichiers PHP et HTML
AddType application/x-httpd-php .php .html

# Charger le module PHP
LoadModule php_module "C:/php/php8apache2_4.dll"

# Spécifier le répertoire du fichier de configuration PHP
PHPIniDir "C:/php"

# Définir l'index par défaut pour les répertoires
DirectoryIndex index.php
```

Remplacez "chemin/vers/module_php" par le chemin réel du répertoire du module PHP, et "chemin/vers/php" par le chemin réel du répertoire de configuration PHP.

Après avoir apporté ces modifications, redémarrez Apache pour appliquer la configuration.

```bash
# Redémarrer Apache
httpd -k restart
```

Assurez-vous d'ajuster les chemins en fonction de vos répertoires d'installation spécifiques.

## Livrable
- [Fichier de configuration Apache par défaut](httpd(par-défaut).conf)
- [Fichier de configuration Apache modifié](httpd(modifié).conf)


## Références

- [Comment installer Apache sur Windows](https://www.sitepoint.com/how-to-install-apache-on-windows/)
- [Comment installer PHP sur Windows](https://www.sitepoint.com/how-to-install-php-on-windows/#step5configurephpasanapachemodule)
- [Tutoriel de configuration Apache](https://www.youtube.com/watch?v=cBa87N_BZ4s&ab_channel=BoostMyTool)
- [Tutoriel d'installation HTTPS](https://www.youtube.com/watch?v=7KHEmFJv4VE&ab_channel=tutortechie)