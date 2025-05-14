# 📘 Manual d'Instal·lació d'una Aplicació Web amb Apache2, MySQL i PHP

Aquest manual descriu el procés per instal·lar una aplicació web dins d'un contenidor Linux (o màquina virtual) utilitzant **Apache2**, **MySQL** i **PHP**, amb la configuració i permisos adequats.

---

## 1️⃣ Instal·lació de PHP 7.4 a Ubuntu 24.04

### Pas 1: Instal·lar els requisits previs de PPA

```bash
sudo apt install software-properties-common -y
```

![Texto alternatiu](1.png)

### Pas 2: Afegir el repositori de PHP 7.4

```bash
LC_ALL=C.UTF-8 sudo add-apt-repository ppa:ondrej/php -y
```

![Texto alternatiu](2.png)

### Pas 3: Actualitzar els repositoris

```bash
sudo apt update
```

![Texto alternatiu](3.png)

### Pas 4: Instal·lar PHP 7.4

```bash
sudo apt install php7.4 -y
```

![Texto alternatiu](4.png)

### Pas 5: Instal·lar PHP i el mòdul per Apache

```bash
sudo apt install -y php libapache2-mod-php7.4
```

![Texto alternatiu](5.png)

### Pas 6: Instal·lar extensions de PHP

```bash
sudo apt install -y php7.4-fpm php7.4-common php7.4-mbstring php7.4-xmlrpc php7.4-soap php7.4-gd php7.4-xml php7.4-intl php7.4-mysql php7.4-cli php7.4-ldap php7.4-zip php7.4-curl
```

![Texto alternatiu](6.png)

### Pas 7: Configurar la versió de PHP per defecte

```bash
sudo update-alternatives --config php
```

![Texto alternatiu](7.png)

### Pas 8: Activar mòduls d'Apache

```bash
sudo a2enmod proxy_fcgi setenvif
```

![Texto alternatiu](8.png)

```bash
sudo a2enconf php7.4-fpm
```

![Texto alternatiu](f.png)

### Pas 9: Reiniciar Apache2

```bash
sudo service apache2 restart
```

![Texto alternatiu](9.png)


Ahora la instalación de owncloud

sudo apt update
![Texto alternatiu](1.1.png)

sudo apt upgrade
![Texto alternatiu](2.1.png)

sudo apt install -y apache2
![Texto alternatiu](3.1.png)

sudo apt install -y mysql-server
![Texto alternatiu](4.1.png)

sudo apt install -y php libapache2-mod-php
![Texto alternatiu](5.1.png)

sudo apt install -y php-fpm php-common php-mbstring php-xmlrpc php-soap php-gd php-xml php-intl php-mysql php-cli php-ldap php-zip php-curl
![Texto alternatiu](larga.png)

sudo systemctl restart apache2
![Texto alternatiu](error.png)


sudo mysql
![Texto alternatiu](sudo mykl.png)



