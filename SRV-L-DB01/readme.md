### SRV-L-DB01
O intuito desses documentos é criar um provisionamento sem falhas e seguro do mariadb para comportar as bases do Zabbix, GLPI e uma base para MremoteNG. Para que funcione sem problemas é importante seguir os passos abaixo:

[install-bd01](https://github.com/idealista07/homelab/blob/main/SRV-L-DB01/install-bd01.md) - Passos para instalação
<br> [database.md](https://github.com/idealista07/homelab/blob/main/SRV-L-DB01/database.md) - Passos para criação das bases
<br> [database-config](https://github.com/idealista07/homelab/blob/main/SRV-L-DB01/database-config.md) - Passos para configuração das bases
<br> [mysqld.cnf](https://github.com/idealista07/homelab/blob/main/SRV-L-DB01/mysqld.cnf) - arquivo de configurações personalizado
<br>
<br> Depois de criado é necessario reiniciar o serviço para aplicar as configurações
```
sudo systemctl restart mysql
```
Para conexão com o zabbix usaremos o arquivo [zabbix-connection](https://github.com/idealista07/homelab/blob/main/SRV-L-DB01/zabbix-connection.md)
