### Instalando o GLPI e suas dependencias 
##### Atualizando os pacotes existentes
```
sudo apt update -y && sudo apt upgrade -y
```
#### Mudando fuso horario para o correto. No meu caso se aplica o fuso de America/Sao_Paulo
```
sudo dpkg-reconfigure tzdata
```
#### Instalando todos os pacotes de dependencia para instalação do GLPI, o comando foi dividido para facilitar a visualização
```
sudo apt-get install apache2 php-cli php-mysql php-xml openssl libapache2-mod-php php-xmlwriter
```
```
sudo apt-get install php-curl php-gd php-intl php-mysqli php-bz2 php-zip php-exif php-xmlreader 
```
```
sudo apt-get install php-dom php-fileinfo php-json php-simplexml php-ldap php-opcach
```
#### Editar arquivo [php.ini]() removendo comentarios do opcache, ou pode-se substituir pelo arquivo contido nesse repositorio
```
sudo vi /etc/php/8.3/apache2/php.ini
```
#### Instalando o GLPI
<br> acessando pasta tmp
```
cd /tmp
```
<br> baixando arquivos de instalação
```
wget https://github.com/glpi-project/glpi/releases/download/10.0.16/glpi-10.0.16.tgz
```
<br> descompactando glpi
```
tar -xvzf glpi-10.0.16.tgz
```
<br> Copiando diretorio descompactado para /var/www/html
```
cp -Rf glpi /var/www/html
```
