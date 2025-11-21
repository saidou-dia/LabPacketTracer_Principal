# Network Lab – Inter-VLAN Routing avec Router-on-a-Stick

## Description
Ce lab simule un réseau d'entreprise simple avec :
- 3 PC dans le VLAN 10
- 3 PC dans le VLAN 20
- 1 serveur dans le VLAN 30
- 2 switches (Switch0 et Switch2)
- 1 routeur (Router0) configuré en router-on-a-stick

L’objectif est de pratiquer :
- Le routage inter-VLAN
- La configuration des trunks et ports access
- La configuration SSH et VLAN management
- L’utilisation des helper-address pour le DHCP

---

## Topologie
- **Router0** → trunk vers Switch0  
- **Switch0** → VLAN 10 et 20 pour les PC, trunks vers Router0 et Switch2  
- **Switch2** → VLAN 10, 20 et 30 pour extension et serveur  
- **VLAN 40** → Management VLAN pour SSH sur les switches

📌 Diagramme dans /diagrams/topo.png

---

## VLANs et IP
| VLAN | Subnet          | Gateway           | Devices            |
|------|----------------|-----------------|------------------|
| 10   | 192.168.10.0/24 | 192.168.10.254  | 3 PC VLAN10       |
| 20   | 192.168.20.0/24 | 192.168.20.254  | 3 PC VLAN20       |
| 30   | 192.168.30.0/24 | 192.168.30.254  | 1 Server VLAN30   |
| 40   | 192.168.40.0/24 | 192.168.40.254  | Management VLAN   |

---

## Configuration rapide
Les fichiers de configuration sont disponibles dans le dossier `configs/` :

- `router0.cfg` → configuration des sous-interfaces, IP, helper-address
- `switch0.cfg` → VLANs, ports access, trunk et VLAN 40 management
- `switch2.cfg` → VLANs, ports access, trunk et VLAN 40 management

---

## SSH et comptes
Tous les devices ont SSH activé sur les lignes VTY avec le compte suivant :  
- **Username:** admin  
- **Password:** cisco  
- **Enable Secret:** cisco

---

## Objectifs pédagogiques
1. Comprendre et configurer le routage inter-VLAN.  
2. Configurer correctement les trunks et les ports access.  
3. Tester la connectivité entre PC, serveur et VLANs.  
4. Configurer l’accès SSH sécurisé sur les switches.  
5. Préparer un lab professionnel pour GitHub/LinkedIn.
