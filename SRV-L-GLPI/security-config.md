#### Criação de pastas seguras para a pasta do GLPI
```
sudo mkdir /var/glpi_data
```
```
sudo mkdir /var/glpi_log
```
#### Movendo arquivos do GLPI para diretorio seguro
```
sudo mv /var/www/html/glpi/files/* /var/glpi_data
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
#### Proteção de cookies no arquivo [based_config.php](https://github.com/idealista07/homelab/blob/main/SRV-L-GLPI/based_config.php)
```
vi /var/www/html/glpi/inc/based_config.php
```
```
ini_set('session.cookie_httponly', 1);
```
#### Apontamento dos diretorios, para reforçar a segurança no arquivo [local_define.php](https://github.com/idealista07/homelab/blob/main/SRV-L-GLPI/local_define.php)
```
vi /var/www/html/glpi/config/local_define.php
```
