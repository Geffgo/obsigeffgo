---
{"dg-publish":true,"permalink":"/commande-chown/"}
---


[[Page d'accueil\|Page d'accueil]]
# COMMANDE chown
### **DÉFINITION**
La commande **`chown`** (change owner) est utilisée sous Linux et Unix pour changer le propriétaire et/ou le groupe d'un fichier ou d'un répertoire. Elle permet à l'administrateur système de modifier la propriété d'un fichier, ce qui est essentiel pour contrôler les accès au système de fichiers.

---

### **UTILITÉ**
- **Changer le propriétaire** : Permet de modifier le propriétaire d'un fichier ou répertoire.
- **Changer le groupe** : Permet de modifier le groupe associé à un fichier ou répertoire.
- **Modification en masse** : Peut être utilisée pour appliquer des changements de propriétaire ou de groupe à plusieurs fichiers en même temps.
  
---

### **COMMANDE**
```bash
sudo chown [OPTION]... [PROPRIETAIRE]:[GROUPE] FICHIER...
```
- **`PROPRIETAIRE`** : Spécifie l'utilisateur auquel le fichier ou répertoire doit appartenir.
- **`GROUPE`** : Spécifie le groupe auquel le fichier ou répertoire doit être associé (optionnel).
- **`FICHIER`** : Le ou les fichiers dont la propriété doit être modifiée.

### **OPTIONS COMMUNES**

- **`-R`** : Applique récursivement le changement de propriétaire et de groupe à tous les fichiers et répertoires à l'intérieur du répertoire spécifié.
  ```bash
  sudo chown -R user1:group1 /home/user1
  ```

- **`-v`** : Affiche des informations détaillées sur les changements effectués.
  ```bash
  sudo chown -v user1 fichier.txt
  ```

- **`--reference=FICHIER`** : Change le propriétaire et le groupe d'un fichier pour les mêmes valeurs que celles du fichier spécifié.
  ```bash
  sudo chown --reference=source.txt target.txt
  ```

---

### **REMARQUES IMPORTANTES**

- **Propriétaire vs Groupe** : Le **propriétaire** est l'utilisateur qui a un contrôle total sur le fichier. Le **groupe** est un ensemble d'utilisateurs ayant certains droits d'accès au fichier.
- **Permissions par défaut** : Si le groupe n'est pas spécifié, le groupe du fichier restera inchangé. Si le propriétaire n'est pas spécifié, il restera inchangé.
- **Utilisation en sécurité** : Le changement de propriétaire ou de groupe peut être utilisé pour gérer les accès et les permissions des utilisateurs dans un environnement multi-utilisateurs, ce qui est une pratique importante pour la gestion de la sécurité.

