#### Criação de pastas seguras para a pasta do GLPI
```
sudo mkdir /var/glpi_data
```
```
sudo mkdir /var/glpi_log
```

#### Mudando permissões dos diretorios
```
chmod 775 /var/www/html/* -Rf
```
```
chmod 775 /var/glpi_data/ -Rf
```
```
chmod 775 /var/glpi_log/ -Rf
```
#### Mudando dono dos diretorios
```
chown www-data /var/www/html/* -Rf
```
```
chown www-data /var/glpi_data/ -Rf
```
```
chown www-data /var/glpi_log/ -Rf
```
#### Proteção de cookies no php
```
vi /var/www/html/glpi/inc/based_config.php
```
```
ini_set('session.cookie_httponly', 1);
```
