---
{"dg-publish":true,"permalink":"/commande-adduser/"}
---


[[Page d'accueil\|Page d'accueil]]
# COMMANDE adduser
### **DÉFINITION**
La commande **`adduser`** est utilisée dans les systèmes Unix/Linux pour créer un nouvel utilisateur. Elle permet de créer un utilisateur, de lui assigner un répertoire personnel, un groupe et d'autres paramètres associés à l'utilisateur, en utilisant une interface simple et interactive.

Cette commande est souvent utilisée par les administrateurs systèmes pour ajouter de nouveaux utilisateurs dans le système, en particulier dans les distributions Linux qui utilisent `adduser` comme une commande de haut niveau (souvent un script qui utilise la commande `useradd` en arrière-plan).

---

### **UTILITÉ**
- **Créer un utilisateur** : Permet d'ajouter un utilisateur avec un répertoire personnel et une configuration de base.
- **Gestion des utilisateurs** : Assure la création de comptes utilisateurs avec des paramètres standard comme le mot de passe, les groupes, et le répertoire.
- **Configuration interactive** : La commande demande des informations comme le mot de passe et d'autres détails liés à l'utilisateur, ce qui simplifie la gestion.

---

### **COMMANDE**
```bash
sudo adduser nom_utilisateur
```

- **`nom_utilisateur`** : Le nom de l'utilisateur à ajouter.

---

### **EXEMPLES D'UTILISATION**

1. **Créer un utilisateur "john"**
   ```bash
   sudo adduser john
   ```
   - Cette commande crée un utilisateur nommé "john" et crée également son répertoire personnel `/home/john`, lui attribue un groupe par défaut, et lui demande un mot de passe.

2. **Créer un utilisateur sans qu'il soit ajouté au groupe sudo (pas de privilèges élevés)**
   ```bash
   sudo adduser --no-create-home john
   ```
   - Crée l'utilisateur "john" sans créer son répertoire personnel, et sans lui attribuer d'autres configurations.

3. **Attribuer un mot de passe lors de la création de l'utilisateur**
   Lors de la création de l'utilisateur, le système demande un mot de passe pour l'utilisateur nouvellement créé.

4. **Ajouter un utilisateur à un groupe spécifique lors de la création**
   Pour ajouter un utilisateur à un groupe lors de sa création, on peut utiliser l'option `-G` :
   ```bash
   sudo adduser john sudo
   ```
   - Cette commande ajoute l'utilisateur "john" au groupe "sudo" immédiatement après sa création, ce qui lui accorde des privilèges d'administration.

---

### **OPTIONS COMMUNES**

- **`--home`** : Spécifie le chemin du répertoire personnel de l'utilisateur.
  ```bash
  sudo adduser --home /custom/path john
  ```

- **`--ingroup`** : Crée un utilisateur et l'ajoute à un groupe spécifique.
  ```bash
  sudo adduser --ingroup developers john
  ```

- **`--shell`** : Définit le shell par défaut pour l'utilisateur.
  ```bash
  sudo adduser --shell /bin/bash john
  ```

- **`--disabled-password`** : Crée un utilisateur sans mot de passe.
  ```bash
  sudo adduser --disabled-password john
  ```

- **`--gecos`** : Permet de définir des informations supplémentaires comme le nom complet de l'utilisateur, son numéro de téléphone, etc.
  ```bash
  sudo adduser --gecos "John Doe,123-456-7890" john
  ```

---

### **REMARQUES IMPORTANTES**
- **Répertoire personnel** : Par défaut, `adduser` crée un répertoire personnel pour l'utilisateur sous `/home/nom_utilisateur`. Ce répertoire est essentiel pour stocker les fichiers personnels de l'utilisateur.
- **Mot de passe** : Il est essentiel de définir un mot de passe lors de la création de l'utilisateur, sauf si l'option `--disabled-password` est utilisée, ce qui crée un utilisateur sans mot de passe.
- **Permissions** : L'utilisateur créé par **`adduser`** peut être ajouté à des groupes supplémentaires (comme `sudo`) en fonction des privilèges qui lui sont attribués.