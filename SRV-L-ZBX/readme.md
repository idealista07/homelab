#### Hostname = SRV-L-ZBX
##### Contendo o Zabbix Server e o Zabbix Agent passivo que será explicado ao longo desses documentos.
##### O intuito desses documentos é criar um provisionamento sem falhas e seguro do zabbix 7.0:

##### Para que funcione sem problemas é importante seguir os passos abaixo:
###### [install-zbx.md]()
###### [/etc/zabbix/zabbix_server.conf]()
###### Agora iremos reiniciar o serviço e habilitar para que iniciem junto com o sistema operacional
```
systemctl restart zabbix-server zabbix-agent apache2
systemctl enable zabbix-server zabbix-agent apache2
```

###### [firewall-zbx.md]()
###### [/etc/zabbix/zabbix_agentd.conf]()
###### [/etc/apache2/sites-available/zabbix.conf]()

###### habilitar a configuração criada
```
sudo a2ensite zabbix.conf
sudo a2enmod rewrite
```
###### Reiniciar serviço do Apache
```
systemctl restart apache2.service
```
