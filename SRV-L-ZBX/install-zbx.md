### Instalando o zabbix e suas dependencias 
##### Atualizando os pacotes existentes
```
sudo apt update -y && sudo apt upgrade -y
```
#### Mudando fuso horario para o correto. No meu caso se aplica o fuso de America/Sao_Paulo
```
sudo dpkg-reconfigure tzdata
```
#### baixamos o pacote do zabbix 7.0
```
sudo wget https://repo.zabbix.com/zabbix/7.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_7.0-2+ubuntu24.04_all.deb
```
#### Instalando o pacote do Zabbix 7.0
```
sudo dpkg -i zabbix-release_7.0-2+ubuntu24.04_all.deb
```
#### Atualizando os pacotes com novas dependencias recem instaladas
```
sudo apt update
```
#### Instalando pacotes necessarios para funcionamento
```
sudo apt install zabbix-frontend-php zabbix-apache-conf zabbix-sql-scripts zabbix-agent
```
configurar arquivo /etc/zabbix/zabbix_server.conf
