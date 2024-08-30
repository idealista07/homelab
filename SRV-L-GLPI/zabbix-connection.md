#### Instalando Agente Zabbix
```
sudo wget https://repo.zabbix.com/zabbix/6.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_6.0-6+ubuntu24.04_all.deb && sudo dpkg -i zabbix-release_6.0-6+ubuntu24.04_all.deb
```
```
sudo apt-get update 
```
```
sudo apt-get install zabbix-agent
```
#### Configurando Agente Zabbix
```
sudo vi /etc/zabbix/zabbix_agentd.conf
```

hostname=[nome da maquina cliente]
server=[ip zabbix]
```
systemctl restart zabbix-agent.service
```
