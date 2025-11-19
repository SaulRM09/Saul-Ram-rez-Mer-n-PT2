# Guia d’instal·lació i configuració de Nextcloud
En aquest apartat explicaré com instal·lar Nextcloud en un entorn on ja disposeu d’un virtual host actiu que apunti a ```/var/www/domini.local```.
## Descàrrega i instal·lació de la plataforma cloud
Aquí haurem d’accedir a l’enllaç indicat. En el moment de fer-hi clic, el fitxer començarà a descarregar-se automàticament.

### 1.1. Enllaços 
- **Nextcloud**: [https://download.nextcloud.com/server/releases/latest.zip](https://download.nextcloud.com/server/releases/latest.zip
  
### 1.2. Passos d’instal·lació

1. **Mou’t al directori del virtual host**:
   ```bash
   cd /var/www/domini.local
   ```
2. **Neteja el contingut actual** (si cal):
   > Assegura’t que no hi ha dades importants abans d’executar això.
   ```bash
   sudo rm -rf *
   ```
   
3. **Descarrega el fitxer `.zip`** de la plataforma triada (Nextcloud o ownCloud) al teu sistema.
    ```bash
    wget https://download.nextcloud.com/server/releases/latest.zip
   ```



---

