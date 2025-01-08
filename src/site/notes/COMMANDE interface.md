---
{"dg-publish":true,"permalink":"/commande-interface/"}
---


[[Page d'accueil\|Page d'accueil]]
# COMMANDE interface
### **UTILITÉ**
La commande **`interface`** permet de configurer une interface spécifique sur un appareil Cisco. Cela inclut les interfaces physiques (comme Ethernet) et les interfaces virtuelles (comme VLAN).

### **COMMANDE**
```
interface INTERFACE_TYPE INTERFACE_NUMBER
```
**INTERFACE_TYPE** : Type d'interface (ex : `GigabitEthernet`, `FastEthernet`, `Serial`, `Vlan`).
**INTERFACE_NUMBER** : Numéro de l'interface (ex : `0/1`, `1/0`, `10`).

### **EXEMPLE D'UTILISATION**
 **Accéder à une interface Ethernet** :
   ```
   Router# configure terminal
   Router(config)# interface GigabitEthernet0/1
   Router(config-if)#
   ```

**Accéder à une interface VLAN** :
   ```
   Router# configure terminal
   Router(config)# interface Vlan10
   Router(config-if)#
   ```

### **COMMANDES COURANTES EN MODE D'INTERFACE**
ip address ADRESSE MASK: Configure l'adresse IP et le masque de sous-réseau de l'interface.
[[COMMANDE no shutdown\|COMMANDE no shutdown]] : Active l'interface (par défaut, certaines interfaces peuvent être désactivées).

### **REMARQUES IMPORTANTES**
Les modifications effectuées dans le mode d'interface ne prennent effet qu'après l'exécution de la [[COMMANDE no shutdown\|COMMANDE no shutdown]].
Pour revenir au mode de configuration global, utilise la commande `exit`.
