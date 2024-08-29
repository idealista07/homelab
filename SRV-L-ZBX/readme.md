#### SRV-L-ZBX
<!-- Arquivos contidos no /etc são gerados apos a instalação dos pacotes -->
<!-- Arquivos .md são sequencia de comandos para seguidos, exceto quando mencionado sua criação -->
O intuito desses documentos é criar um provisionamento sem falhas e seguro do zabbix 7.0 no projeto apresentado será usado os serviços "Zabbix Server" e o "Zabbix Agent" de modo passivo no mesmo servidor.
Arquivos manipulados:
<br>
<br> [install-zbx.md](https://github.com/idealista07/homelab/blob/main/SRV-L-ZBX/install-zbx.md) - Passos para instalação
<br> [/etc/zabbix/zabbix_server.conf](https://github.com/idealista07/homelab/blob/main/SRV-L-ZBX/zabbix_server.conf) - Configurando banco de dados no servidor Zabbix
<br> [firewall-zbx.md](https://github.com/idealista07/homelab/blob/main/SRV-L-ZBX/firewall-zbx.md) - Liberação de portas
<br> [/etc/zabbix/zabbix_agentd.conf](https://github.com/idealista07/homelab/blob/main/SRV-L-ZBX/zabbix_agentd.conf) - Configurando agente zabbix
<br> [/etc/apache2/sites-available/zabbix.conf](https://github.com/idealista07/homelab/blob/main/SRV-L-ZBX/zabbix.conf) - Configuração centralizada para apache2

##### Para que funcione sem problemas é importante seguir os passos abaixo:
Inicie a instalação com os passos no documento [install-zbx.md](https://github.com/idealista07/homelab/blob/main/SRV-L-ZBX/install-zbx.md) e edite o documento [/etc/zabbix/zabbix_server.conf](https://github.com/idealista07/homelab/blob/main/SRV-L-ZBX/zabbix_server.conf) alterando os seguintes campos:
<br> <br> DBHost=[ip do banco de dados] linha 83
<br> DBUser=[usuario] linha 111
<br> DBPassword=[senha] linha 119
<br> DBName=[nome do banco] linha 93
###### Agora iremos reiniciar o serviço e habilitar para que iniciem junto com o sistema operacional
```
systemctl restart zabbix-server zabbix-agent apache2
systemctl enable zabbix-server zabbix-agent apache2
```
Libere as portas no firewall para funcionamento dos serviços usando os passos no arquivo [firewall-zbx.md](https://github.com/idealista07/homelab/blob/main/SRV-L-ZBX/firewall-zbx.md) 

Edite o arquivo [/etc/zabbix/zabbix_agentd.conf](https://github.com/idealista07/homelab/blob/main/SRV-L-ZBX/zabbix_agentd.conf) para configurar o agente passivo, alterando as seguintes informações:
<br> 
<br> hostname=[nome da maquina cliente]
<br> server=[ip zabbix]
<br> 
<br> Toda alteração realizada nesse arquivo é necessario reiniciar o serviço
```
sudo systemctl restart zabbix-agent
```
<!-- Esse arquivo é criado do zero para ajustes de segurança no ambiente que utiliza apache -->
<br> Para ter um bom desempenho, segurança e uma configuração centralizada criei esse arquivo [/etc/apache2/sites-available/zabbix.conf](https://github.com/idealista07/homelab/blob/main/SRV-L-ZBX/zabbix.conf)

###### habilitar a configuração criada no arquivo zabbix.conf
```
sudo a2ensite zabbix.conf
sudo a2enmod rewrite
```
<br> Toda alteração realizada nesse arquivo é necessario reiniciar o serviço do Apache
```
systemctl restart apache2.service
```
