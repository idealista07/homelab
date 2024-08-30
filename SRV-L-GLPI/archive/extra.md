### Passos para instalar o plugin do Custom login no GLPI, responsavel por personalização de logo e wallpaper na tela inicial dop GLPI

#### Baixando os arquivos
```
sudo git clone https://github.com/serviceticst/glpi-plugin-custom_login.git
```
#### Descompactando
```
sudo unzip glpijccustomlogin.zip 
```
#### Acessando diretorio
```
cd glpi-plugin-custom_login
```
#### Movendo arquivos
```
sudo mv glpijccustomlogin /docker/projeto/storage/www/html/glpi/plugins
```
#### Removendo lixo
```
sudo rm -r README glpijccustomlogin.zip glpi-plugin-custom_login
```
#### Instalando dependencias
```
sudo apt update && sudo apt install php-gd php-curl php-xml composer php-fpm php-json php-mbstring mysql-server php-mysql php-mysqli
```
#### VERIFICAR
```
sudo composer update
```
