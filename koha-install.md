# koha-install

## 1. Instalar mariadb:
sudo apt-get install mariadb-server -y

## 2. Añadir el repositorio koha:
wget -q -O- http://debian.koha-community.org/koha/gpg.asc | sudo apt-key add -

echo 'deb http://debian.koha-community.org/koha stable main' | sudo tee /etc/apt/sources.list.d/koha.list

## 3. Instalar koha:
sudo apt-get install koha-common

## 4. configurar koha-sites: 
sudo nano /etc/koha/koha-sites.conf


![alt text](koha-sites.png?raw=true)

## 5. configuracion de apache:
sudo a2enmod rewrite

sudo a2enmod cgi

###Después ya podemos reiniciar el servidor con el comando:

sudo service apache2 restart
