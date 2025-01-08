---
{"dg-publish":true,"permalink":"/commande-configure-terminal/"}
---


[[Page d'accueil\|Page d'accueil]]
# COMMANDE configure terminal
### **UTILITÉ**
La commande **`configure terminal`** permet d'accéder au mode de configuration global d'un appareil Cisco. Ce mode permet de modifier la configuration de l'appareil.

### **COMMANDE**
```
configure terminal
```

### **TYPE DE MODE**
- **Mode Privilégié** : Pour entrer dans le mode de configuration, tu dois d'abord être en mode privilégié (après avoir utilisé la [[COMMANDE enable\|commande enable]]).

### **EXEMPLE D'UTILISATION**
 **Accéder au mode de configuration global** :
   ```
   Router# configure terminal
   Router(config)#
   ```
Après avoir entré la commande, un prompt `(config)#` indique que tu es maintenant en mode de configuration.

### **COMMANDES COURANTES EN MODE DE CONFIGURATION**
**`hostname NOM`** : Définit le nom de l'appareil.
[[COMMANDE interface\|COMMANDE interface]] INTERFACE : Accède à la configuration d'une interface spécifique (ex. `interface GigabitEthernet0/1`).
[[COMMANDE exit\|COMMANDE exit]] : Sort du mode de configuration courant pour revenir au mode précédent.