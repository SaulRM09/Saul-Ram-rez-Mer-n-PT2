# Saul-Ram-rez-Mer-n-PT2
## Manual d'instal·lació d’ownCloud amb virtualització mitjançant IsardVDI ##
---
### 1. Configuració del sistema de virtualització (IsardVDI)
En primer lloc, hauríem de tenir una sessió iniciada a IsardVDI per poder crear la màquina virtual. Per crear la màquina virtual, hem d’anar a la icona blava on diu **“Escriptori nou”**. Dins d’aquest apartat, hauríem de buscar **“ubuntu-24.04-desktop”**. Després d’això, li posem el nom que vulguem al nou escriptori i l’iniciem.

### 2. Configurar una màquina virtual per allotjar ownCloud
Després d’haver creat la màquina virtual, cal preparar l’entorn perquè sigui possible instal·lar-hi ownCloud. Per fer-ho, haurem de seguir els passos que s’indiquen a continuació. Per començar, obrirem el nostre terminal i executarem les ordres següents.

### 2.1 Actualitza el sistema
```bash
sudo apt update && sudo apt upgrade -y
```

### 2.2 Instal·la Apache
```bash
sudo apt install apache2 -y
```
#### Activa i inicia el servei:
```bash
sudo systemctl enable apache2
sudo systemctl start apache2
```
#### Verifica l’estat:
```bash
sudo systemctl status apache2
```
Visita ```http://localhost``` per veure la pàgina per defecte d’Apache.

### 2.3 Instal·la MySQL
Ubuntu 24.04 ja inclou el paquet ```mysql-server``` als repositoris oficials (versió 8.0 o superior):
```bash
sudo apt install mysql-server mysql-client -y
```
#### Inicia i habilita el servei:
```bash
sudo systemctl enable mysql
sudo systemctl start mysql
```
#### Configura de MySQL:
#### Accés a la consola de MySQL
```bash
sudo mysql
```
#### Creació de la base de dades
```bash
CREATE DATABASE bbdd;
```
#### Creació de l’usuari local
```bash
CREATE USER 'usuario'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
GRANT ALL PRIVILEGES ON bbdd.* TO 'usuario'@'localhost';
FLUSH PRIVILEGES;
EXIT;
```
>  ⚠️ **NOTA:** Aquest usuari només pot connectar-se des del servidor local (```localhost```), cosa que és suficient si l’aplicació web i la base de dades estan al mateix servidor.





---
#### 3. Instal·lació del gestor d’arxius Nextcloud:



   
