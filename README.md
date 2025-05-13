# 📘 Manual d'Instal·lació d'una Aplicació Web amb Apache2, MySQL i PHP

Aquest manual descriu el procés per instal·lar una aplicació web dins d'un contenidor Linux (o màquina virtual) utilitzant **Apache2**, **MySQL** i **PHP**, amb la configuració i permisos adequats.

---

## 🔧 Actualització del sistema

```bash
sudo apt update
sudo apt upgrade
```

---

## 🌐 Instal·lació d'Apache2

```bash
sudo apt install -y apache2
```

Apache2 utilitza per defecte el directori següent com a **directori arrel** del servidor web:

```
/var/www/html
```

Qualsevol fitxer que hi posem serà accessible des del navegador amb:

```
http://localhost
```

---

## 🗃️ Instal·lació de MySQL

```bash
sudo apt install -y mysql-server
```

---

## 🧩 Instal·lació de PHP i llibreries recomanades

```bash
sudo apt install -y php libapache2-mod-php
sudo apt install -y php-fpm php-common php-mbstring php-xmlrpc php-soap php-gd \
php-xml php-intl php-mysql php-cli php-ldap php-zip php-curl
```

---

## 🔁 Reinici del servidor Apache2

```bash
sudo systemctl restart apache2
```

---

## 🛠️ Configuració de MySQL

### Accedir a la consola MySQL

```bash
sudo mysql
```

### Crear una base de dades

```sql
CREATE DATABASE bbdd;
```

### Crear un usuari local

```sql
CREATE USER 'usuario'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
GRANT ALL ON bbdd.* TO 'usuario'@'localhost';
```

### Sortir de MySQL

```sql
exit
```

### Comprovar connexió amb l'usuari nou

```bash
mysql -u usuario -p
```

---

## 📦 Desplegament de l'aplicació web

### Copiar l’arxiu ZIP de l’aplicació

```bash
sudo cp ~/Baixades/app-web.zip /var/www/html
```

### Anar al directori arrel del servidor web

```bash
cd /var/www/html
```

### Descomprimir el fitxer ZIP

```bash
sudo unzip app-web.zip
```

### Moure els fitxers descomprimits a `/var/www/html`

```bash
sudo cp -R app-web/. /var/www/html
```

### Eliminar la carpeta temporal creada per l’unzip

```bash
sudo rm -rf app-web/
```

### Eliminar la pàgina per defecte d’Apache

```bash
sudo rm -rf /var/www/html/index.html
```

---

## 🔐 Aplicació de permisos

```bash
cd /var/www/html
sudo chmod -R 775 .
sudo chown -R usuario:www-data .
```

---

## ✅ Accés a l'aplicació

Un cop tot estigui configurat i els serveis estiguin en funcionament, pots accedir a l'aplicació des del navegador:

```
http://localhost
```

---

### 🔁 Notes finals:
- Substitueix **`usuario`** pel teu nom d’usuari real.
- Substitueix **`app-web.zip`** pel nom real del teu fitxer ZIP.
- Revisa que les rutes siguin correctes segons el teu idioma del sistema (per exemple, `Baixades` pot ser `Downloads` si el sistema està en anglès).
