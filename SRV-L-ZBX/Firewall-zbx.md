### IMPORTANTE 
#### Liberar portas 80 e 443 no firewall e 10051 apenas na rede
#### Atualmente o serviço sai da minha casa para uma VPN na Oracle Cloud e redirecionado para Cloudflare proteger com SSL por conta disso mantenho as portas 80 e 443 abertas e a 10051 apenas para rede.

##### Liberando porta 80
```
sudo ufw allow to any port 80
```
##### Liberando porta 443
```
sudo ufw allow to any port 443
```
##### Liberando porta 10051
```
sudo ufw allow from 172.16.30.0/24 to any port 10051
```
##### Habilitando serviço
```
sudo ufw enable
```


