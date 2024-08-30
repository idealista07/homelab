### SRV-L-GLPI
O intuito desses documentos é criar um provisionamento sem falhas e seguro do GLPI para comportar a interface do ITSM. Para que funcione sem problemas é importante seguir os passos abaixo:

[Install-glpi](https://github.com/idealista07/homelab/blob/main/SRV-L-GLPI/install-glpi.md) - Passos para instalação
<br> [Firewall-glpi.md](https://github.com/idealista07/homelab/blob/main/SRV-L-GLPI/firewall-glpi.md) - Passos para configuração do firewall da maquina virtual
<br> [Security-config.md](https://github.com/idealista07/homelab/blob/main/SRV-L-GLPI/security-config.md) - Passos para configuração de segurança do serviço
<br> [Cache-glpi.md](https://github.com/idealista07/homelab/blob/main/SRV-L-GLPI/cache-glpi.md) - arquivo de configurações de cache do GLPI
<br>
<br> Depois de criado é necessario reiniciar o serviço para aplicar as configurações
```
sudo systemctl restart mysql
```
Para conexão com o zabbix usaremos o arquivo [zabbix-connection](https://github.com/idealista07/homelab/blob/main/SRV-L-DB01/zabbix-connection.md)
