#### Gerando backup do arquivo de configuração e editando um para ter melhor desempenho
```
sudo cp /etc/mysql/mysql.conf.d/mysqld.cnf /etc/mysql/mysql.conf.d/mysqld-bkp.cnf
```
```
sudo rm -r /etc/mysql/mysql.conf.d/mysqld.cnf
```
Criando arquivo [mysqld.cnf](https://github.com/idealista07/homelab/blob/main/SRV-L-DB01/mysqld.cnf) para melhor desempenho
```
sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf
```
Necessario reiniciar o serviço para alterações no arquivo
```
sudo systemctl restart mysql
```
Para Configurar a base para melhor segurança e desempenho deve-se seguir os passos abaixo:
```
mysql_secure_installation
```
<br>no
<br>no
<br>y
<br>y
<br>y
<br>y
