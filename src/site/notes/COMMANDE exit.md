---
{"dg-publish":true,"permalink":"/commande-exit/"}
---


[[Page d'accueil\|Page d'accueil]]
# COMMANDE exit
### **UTILITÉ**
La commande **`exit`** est utilisée pour quitter le mode actuel de configuration et revenir au mode précédent dans la hiérarchie de configuration de l'IOS Cisco. Elle permet de naviguer entre les différents modes de l'IOS en sortant d'un niveau pour revenir au niveau supérieur.

### **COMMANDE**
```
exit
```

### **EXEMPLES D'UTILISATION**
   ```bash
   Router(config)# interface gigabitEthernet 0/0
   Router(config-if)# no shutdown
   Router(config-if)# exit
   Router(config)#
   ```
   
### **COMMANDES COMPLÉMENTAIRES**
- **`end`** : Sort du mode de configuration actuel et retourne directement au mode privilégié (`#`) sans passer par les étapes intermédiaires.
- **`logout`** : Utilisé pour fermer la session active de l'utilisateur, souvent dans le cadre d'une connexion distante.

### **REMARQUES IMPORTANTES**
- **`exit`** fonctionne par étapes : elle fait remonter d’un niveau dans la hiérarchie des modes. Pour retourner directement au mode utilisateur privilégié, la commande **`end`** peut être utilisée.
- Si l'utilisateur est dans le mode **console** ou **vty**, la commande **`exit`** met fin à la session de connexion en cours.
