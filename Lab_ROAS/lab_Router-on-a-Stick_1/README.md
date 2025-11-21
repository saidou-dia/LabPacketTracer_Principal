# Network Lab – Routage Inter-VLAN

## Description
Ce lab simule un réseau d’entreprise simple avec :  
- 3 PC dans le VLAN 10  
- 3 PC dans le VLAN 20  
- 1 serveur dans le VLAN 30  
- 2 switches (SW0 et SW1)  
- 1 routeur (R0) configuré en **router-on-a-stick**

L’objectif est de pratiquer :  
- Le routage inter-VLAN  
- La configuration des trunks et ports access  
- La configuration SSH et VLAN management  
- L’utilisation des helper-address pour le DHCP

---

## Topologie
La topologie du lab est disponible dans le dossier `/capture/Topology/` :  
- `Topology.png` → diagramme réseau avec VLANs et connexions trunk/access

- **R0** → trunk vers SW0  
- **SW0** → VLAN 10 et 20 pour les PC, trunk vers R0 et SW1  
- **SW2** → VLAN 10, 20 et 30 pour extension et serveur  
- **VLAN 40** → Management VLAN pour SSH sur les switches

---

## VLANs et IP
| VLAN | Subnet           | Gateway           | Devices             |
|------|-----------------|-----------------|------------------|
| 10   | 192.168.10.0/24 | 192.168.10.254  | 3 PC VLAN10       |
| 20   | 192.168.20.0/24 | 192.168.20.254  | 3 PC VLAN20       |
| 30   | 192.168.30.0/24 | 192.168.30.254  | 1 Server VLAN30   |
| 40   | 192.168.40.0/24 | 192.168.40.254  | Management VLAN   |

---

## Configurations
Les fichiers de configuration sont disponibles dans le dossier `configs/` :  

- `R0.txt` → configuration du routeur avec sous-interfaces et helper-address  
- `SW0.txt` → configuration des VLANs, ports access et trunk, VLAN40 pour management  
- `SW1.txt` → configuration des VLANs, ports access et trunk, VLAN40 pour management  

---

## SSH et comptes
Tous les devices ont SSH activé sur les lignes VTY avec le compte suivant :  
- **Username:** admin  
- **Password:** cisco  
- **Enable Secret:** cisco

---

## Captures d’écran
- `/capture/Empty/PC0_Ping_Fail.png` → ping échoué avant configuration  
- `/capture/Solution/PC0_Ping.png` → ping réussi après configuration  
- `/capture/Solution/R0_show_run.png` → configuration du routeur  
- `/capture/Solution/SW0_show_vlan_trunk.png` → VLAN et trunk sur SW0  

---

## Fichiers Packet Tracer
- `/pkt/Router-on-a-Stick_1_empty.pkt` → fichier initial pour exercice  
- `/pkt/Router-on-a-Stick_1_completed.pkt` → fichier final avec config complète

---

## Objectifs pédagogiques
1. Comprendre et configurer le routage inter-VLAN.  
2. Configurer correctement les trunks et ports access.  
3. Tester la connectivité entre PC et serveur dans différents VLANs.  
4. Configurer un accès SSH sécurisé sur les switches.  
5. Préparer un lab professionnel pour GitHub et LinkedIn.


