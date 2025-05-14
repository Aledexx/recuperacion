# 📘 Manual d'Instal·lació d'una Aplicació Web amb Apache2, MySQL i PHP

Aquest manual descriu el procés per instal·lar una aplicació web dins d'un contenidor Linux (o màquina virtual) utilitzant **Apache2**, **MySQL** i **PHP**, amb la configuració i permisos adequats.


Tendrás que empezar por este comando 
sudo apt install software-properties-common -y

![Texto alternativo](1.png)

LC_ALL=C.UTF-8 sudo add-apt-repository ppa:ondrej/php -y
![Texto alternativo](2.png)

sudo apt update
![Texto alternativo](3.png)

sudo apt install php7.4 -y
![Texto alternativo](4.png)

sudo apt install -y php libapache2-mod-php7.4
![Texto alternativo](5.png)

sudo apt install -y php7.4-fpm php7.4-common php7.4-mbstring php7.4-xmlrpc php7.4-soap php7.4-gd php7.4-xml php7.4-intl php7.4-mysql php7.4-cli php7.4-ldap php7.4-zip php7.4-curl
![Texto alternativo](6.png)

sudo update-alternatives --config php
![Texto alternativo](7.png)

sudo a2enmod proxy_fcgi setenvif
![Texto alternativo](8.png)

sudo a2enconf php7.4-fpm
![Texto alternativo](9.png)

sudo service apache2 restart
![Texto alternativo](10.png)





