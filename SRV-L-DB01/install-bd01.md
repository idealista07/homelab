### Instalando o MariaDB e suas dependencias 
##### Atualizando os pacotes existentes
```
sudo apt update -y && sudo apt upgrade -y
```
#### Mudando fuso horario para o correto. No meu caso se aplica o fuso de America/Sao_Paulo
```
dpkg-reconfigure tzdata
```
#### Cria e acessa o diretorio downloads
```
mkdir /downloads && cd /downloads
```
#### Baixa o pacote .deb para instalação das dependencias
```
sudo wget https://repo.zabbix.com/zabbix/7.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_7.0-2+ubuntu24.04_all.deb
```
#### Instalando o pacote
```
sudo dpkg -i zabbix-release_7.0-2+ubuntu24.04_all.deb
```
#### Atualiza e instala os serviços mysql-server, zabbix-sql-scripts e zabbix-agent
```
sudo apt update && sudo apt install mysql-server zabbix-sql-scripts zabbix-agent
```
