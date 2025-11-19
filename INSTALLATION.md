# Saul-Ram-rez-Mer-n-PT2
## Manual d'instal·lació d’ownCloud amb virtualització mitjançant IsardVDI ##
---
### 1. Configuració del sistema de virtualització (IsardVDI)
En primer lloc, hauríem de tenir una sessió iniciada a IsardVDI per poder crear la màquina virtual. Per crear la màquina virtual, hem d’anar a la icona blava on diu **“Escriptori nou”**. Dins d’aquest apartat, hauríem de buscar **“ubuntu-24.04-desktop”**. Després d’això, li posem el nom que vulguem al nou escriptori i l’iniciem.

### 2. Configurar una màquina virtual per allotjar Nextcloud
Després d’haver creat la màquina virtual, cal preparar l’entorn perquè sigui possible instal·lar-hi Nextcloud. Per fer-ho, haurem de seguir els passos que s’indiquen a continuació. Per començar, obrirem el nostre terminal i executarem les ordres següents.
### 2.1 Actualitza el sistema
```bash
sudo apt update && sudo apt upgrade -y
```
### 2.2 Instal·la Apache
```bash
sudo apt install apache2 -y
```

---
#### 3. Instal·lació del gestor d’arxius Nextcloud:



   
