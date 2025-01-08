---
{"dg-publish":true,"permalink":"/commande-enable/"}
---


[[Page d'accueil\|Page d'accueil]]
# COMMANDE enable
### **UTILITÉ**
La commande **`enable`** est utilisée dans les appareils Cisco IOS pour passer en mode privilégié. Ce mode permet d'exécuter des commandes avancées et de configurer le système.

### **COMMANDE**

``enable [NIVEAU]

``[NIVEAU]`` (optionnel) : Définit le niveau d'accès si la configuration le nécessite (par défaut, c'est le niveau 15).

### **TYPE DE MODE**
**Mode Utilisateur** : Mode par défaut après la connexion, où seules certaines commandes de base sont accessibles.
**Mode Privilégié** : Mode accessible avec la commande `enable`, permettant d'exécuter toutes les commandes de configuration.

### **EXEMPLE D'UTILISATION**

**Passer en mode privilégié** :
   ```
   Router> enable
   Router#
   ```
Après avoir entré la commande, un prompt `#` indique que tu es maintenant en mode privilégié.

**Utilisation d’un mot de passe** :
Si un mot de passe est configuré, il te sera demandé après l'exécution de la commande `enable`.
   ```
   Router> enable
   Password: ********
   Router#
   ```
