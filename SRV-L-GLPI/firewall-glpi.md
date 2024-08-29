## Liberação de portas

Liberando porta 80
```
sudo ufw allow 80/tcp
```
Liberando porta 443
```
sudo ufw allow 443/tcp
```
Liberando porta 22 para rede
```
sudo ufw allow from 172.16.30.0/24 to any port 22
```
Liberando porta 10050 para rede
```
sudo ufw allow from 172.16.30.9 to any port 10050
```
Habilitando Serviço
```
sudo ufw enable
```
