Para monitoramento Zabbix é necessario adicionar arquivo [.my.cnf](https://github.com/idealista07/homelab/blob/main/SRV-L-DB01/.my.cnf) de credenciais para conexão:
```
sudo mkdir /var/lib/zabbix/ && sudo vi /var/lib/zabbix/.my.cnf
```
Criar o template para coleta de dados [template_db_mysql.conf](https://github.com/idealista07/homelab/blob/main/SRV-L-DB01/template_db_mysql.conf)
```
sudo vi /etc/zabbix/zabbix_agent.d/template_db_mysql.conf
```
Configurar o agente Zabbix no arquivo [zabbix_agentd.conf](https://github.com/idealista07/homelab/blob/main/SRV-L-ZBX/zabbix_agentd.conf)
```
sudo vi /etc/zabbix/zabbix_agent/zabbix_agentd.conf
```
