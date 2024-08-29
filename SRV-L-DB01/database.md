### Para usar os comandos abaixo é necessario acessar o banco de dados com o comando 
```
mysql -uroot -p
```
#### Banco do Zabbix
OBS: Se instalar no mesmo servidor deve-se usar o @localhost para restringir apenas acesso local
<br><br>Preencha o nome da base substituindo o nome "zabbix" no primeiro comando e final do terceiro.
<br>Preencha o nome do usuario substituindo o nome "userzabbix" no segundo comando e antes do * do terceiro comando.
<br>Preencha a senha do usuario substituindo o nome "senha" no segundo comando.
```
create database zabbix character set utf8mb4 collate utf8mb4_bin;
```
```
create user userzabbix identified by 'senha';
```
```
grant all privileges on userzabbix.* to zabbix;
```
```
set global log_bin_trust_function_creators = 1;
```
```
FLUSH PRIVILEGES;
```

#### Banco do GLPI
Preencha o nome da base substituindo o nome "glpi" no primeiro comando e final do terceiro.
<br>Preencha o nome do usuario substituindo o nome "userglpi" no segundo comando e antes do * do terceiro comando.
<br>Preencha a senha do usuario substituindo o nome "senha" no segundo comando.
```
create database glpi;
```
```
create user 'userglpi' identified by 'senha';
```
```
grant all privileges on userglpi.* to 'glpi';
```
```
FLUSH PRIVILEGES;
```
#### Usuario Remoto
Preencha o nome do usuario substituindo o nome "remoteuser" e no segundo comando.
<br>Preencha a senha do usuario substituindo o nome "senha" no primeiro comando.
```
CREATE USER 'remoteuser'@'%' IDENTIFIED BY 'senha';
```
```
GRANT ALL PRIVILEGES ON *.* TO 'remoteuser'@'%' WITH GRANT OPTION;
```
```
FLUSH PRIVILEGES;
```
#### Usuario de monitoramento Zabbix
Preencha o nome do usuario substituindo o nome "zbx_monitor" e no segundo comando.
<br>Preencha a senha do usuario substituindo o nome "senha" no primeiro comando.
```
CREATE USER 'zbx_monitor'@'%' IDENTIFIED BY 'senha';
```
```
GRANT REPLICATION CLIENT,PROCESS,SHOW DATABASES,SHOW VIEW ON *.* TO 'zbx_monitor'@'%';
```
```
FLUSH PRIVILEGES;
```
#### Alterando senha do Root
Preencha a senha do usuario substituindo o nome "senharoot" no primeiro comando.
```
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'senharoot';
```
```
FLUSH PRIVILEGES;
```
