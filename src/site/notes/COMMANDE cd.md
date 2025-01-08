---
{"dg-publish":true,"permalink":"/commande-cd/"}
---


[[Page d'accueil\|Page d'accueil]]
# COMMANDE cd
### **UTILITÉ**
La commande **`cd`** (Change Directory) est utilisée pour naviguer entre les répertoires du système de fichiers. Elle permet de se déplacer vers un autre répertoire en spécifiant son chemin relatif ou absolu.

### **COMMANDE**
```
cd [DIRECTORY]
```
- **DIRECTORY** : Chemin vers le répertoire où l'on souhaite se déplacer. Ce chemin peut être **relatif** ou **absolu**.

### **EXEMPLES D'UTILISATION**
**Se déplacer vers un répertoire spécifique** (par exemple, le répertoire `Documents`) :
   ```
   cd Documents
   ```

**Revenir au répertoire parent** :
   ```
   cd ..
   ```

**Se déplacer vers le répertoire personnel de l'utilisateur** :
   ```
   cd ~
   ```

**Se déplacer vers un répertoire en utilisant un chemin absolu** :
   ```
   cd /home/user/Documents
   ```

**Retourner au répertoire précédent** (avant la dernière commande `cd`) :
   ```
   cd -
   ```

### **COMMANDES COMPLÉMENTAIRES**
- [[COMMANDE pwd\|COMMANDE pwd]]: Affiche le chemin actuel dans lequel vous vous trouvez.
- [[COMMANDE ls\|COMMANDE ls]]: Liste le contenu du répertoire dans lequel vous venez d'arriver après la commande `cd`.

### **REMARQUES IMPORTANTES**
Si aucun répertoire n'est spécifié, la commande **`cd`** vous ramène par défaut à votre **répertoire personnel** (`/home/user`).
**`cd ..`** vous fait remonter d'un niveau dans l'arborescence des répertoires.