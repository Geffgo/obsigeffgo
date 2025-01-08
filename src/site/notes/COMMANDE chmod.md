---
{"dg-publish":true,"permalink":"/commande-chmod/"}
---


[[Page d'accueil\|Page d'accueil]]
# COMMANDE chmod
### **UTILITÉ**
La commande **`chmod`** permet de modifier les permissions d'un fichier ou d'un répertoire. Seul l'utilisateur **`root`** ou le propriétaire du fichier peut modifier ces permissions.

### **COMMANDE**
```
chmod [<SET><ACTION><PERMISSIONS>]... FILE
```

### **MÉTHODE SYMBOLIQUE**
**`<SET>`** :
  - **`u`** : User - L’utilisateur propriétaire du fichier
  - **`g`** : Group - Le groupe propriétaire du fichier
  - **`o`** : Others - Toute personne autre que l'utilisateur propriétaire ou un membre du groupe propriétaire
  - **`a`** : All - Désigne l'utilisateur, le groupe et les autres

**`<ACTION>`** :
  - **`+`** : Ajoute la permission si nécessaire
  - **`=`** : Précise la permission exacte
  - **`-`** : Retire la permission si nécessaire
  
**`<PERMISSIONS>`** :
  - **`r`** : read - Lecture
  - **`w`** : write - Écriture
  - **`x`** : execute - Exécution

### **REMARQUES IMPORTANTES**
Pour vérifier les permissions actuelles d'un fichier, utilise la commande `ls -l`.
Les modifications de permissions sont souvent nécessaires pour la sécurité et la gestion des accès aux fichiers.
