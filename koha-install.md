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

(Después ya podemos reiniciar el servidor con el comando):

sudo service apache2 restart

## 6. Crear una instancia de Koha para la biblioteca de nombres

sudo koha-create --create-db library

## 7. Ajuste de seguridad para MySQL

sudo mysql_secure_installation

(Al ejecutar este script, respondí Y (Sí) a todas las demás).

## 8. Añadiendo puertos

sudo nano /etc/apache2/ports.conf

![alt text](ports.png?raw=true)

