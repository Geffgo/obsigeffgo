---
{"dg-publish":true,"permalink":"/c1-arp/"}
---


[[Page d'accueil\|Page d'accueil]]
# C1 ARP
### Explication

Les adresses **MAC (Media Access Control)** sont des <font color="#e36c09">identifiants uniques</font> qui permettent de reconnaître les cartes réseau au sein d'un réseau local. Elles sont<font color="#e36c09"> utilisées pour acheminer les données directement entre appareils d'un même réseau</font>. Les adresses IP, en revanche, sont des adresses logiques qui permettent de localiser des appareils et d'envoyer des données entre différents réseaux.

Le protocole **ARP (Address Resolution Protocol)** <font color="#e36c09">traduit les adresses IP en adresses MAC</font> pour permettre la communication au niveau physique. Lorsqu'un appareil ne connaît pas l'adresse MAC correspondant à une adresse IP, il envoie une requête ARP pour obtenir cette information.

---

### **Exemples**

#### 1. **Communication locale (même réseau)**

**Situation :**  

Un PC avec l'adresse <font color="#e36c09">IP 192.168.1.2</font> et l'adresse<font color="#e36c09"> MAC 00-AA-BB-CC-DD-EE</font> souhaite imprimer un document. 
L'imprimante est connectée au même réseau avec l'adresse <font color="#e36c09">IP 192.168.1.3</font> et l'adresse <font color="#e36c09">MAC 11-22-33-44-55.</font>

**Processus :**

- Le PC utilise l'adresse MAC de l'imprimante pour envoyer directement les données d'impression.
- La communication reste confinée au réseau local.

---

#### 2. **Communication vers un réseau distant**

**Situation :**  
Un utilisateur souhaite accéder à un site web hébergé à l'adresse <font color="#e36c09">IP 203.0.113.5</font>. L'ordinateur de l'utilisateur a l'adresse <font color="#e36c09">IP 192.168.1.2</font> et utilise un routeur avec l'adresse <font color="#e36c09">MAC 00-FF-AA-BB-CC-DD</font> comme passerelle.

**Processus :**

- Le PC envoie les données au routeur en utilisant son adresse MAC.
- Le routeur, après avoir analysé l'adresse IP de destination, transfère les données au réseau suivant en modifiant l'adresse MAC à chaque étape.

---

#### 3. **Protocole ARP**

**Situation :**  
Un ordinateur (<font color="#e36c09">IP : 192.168.1.2</font>) ne connaît pas l'adresse MAC associée à une adresse IP (<font color="#e36c09">192.168.1.3</font>).

**Processus :**

- Une requête ARP est diffusée sur le réseau avec un message du type : <font color="#e36c09">"Qui a l'adresse IP 192.168.1.3 ?"</font>
- L'appareil possédant cette adresse IP (par exemple, l'imprimante) <font color="#e36c09">répond avec son adresse MAC (11-22-33-44-55).</font>
- Cette correspondance est temporairement <font color="#e36c09">stockée dans la table ARP du PC</font> pour des communications ultérieures.
