#### Editar arquivo [php.ini](https://github.com/idealista07/homelab/blob/main/SRV-L-GLPI/php.ini) removendo comentarios do opcache, ou pode-se substituir pelo arquivo contido nesse repositorio
```
sudo vi /etc/php/8.3/apache2/php.ini
```
#### Desabilitar a configuração padrão do Apache
```
a2dissite 000-default
```
#### Criar um arquivo [glpi.conf](https://github.com/idealista07/homelab/blob/main/SRV-L-GLPI/glpi.conf) de configuração centralizada para o GLPi:
```
sudo vi /etc/apache2/sites-available/glpi.conf
```
