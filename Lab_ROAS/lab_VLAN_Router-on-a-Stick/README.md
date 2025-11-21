# CCNA Lab – Routage Inter-VLAN avec Router-on-a-Stick

## 🚀 Objectif

Ce lab a pour but de comprendre et pratiquer le **routage inter-VLAN** avec un routeur en **Router-on-a-Stick**.  
Vous apprendrez à configurer des VLANs sur des switches, à configurer des ports access et trunks, et à vérifier la connectivité entre VLANs.

---

## 💡 Topologie

- **Switches** : SW0, SW1  
- **Routeur** : R1  
- **VLANs** :
  - VLAN 10 (Bleu) – 192.168.10.0/24
  - VLAN 20 (Jaune) – 192.168.20.0/24
  - VLAN 30 (Rouge) – 192.168.30.0/24  
- **Équipements** :
  - PCs et serveur assignés aux VLANs correspondants

![Topo](diagram/topo.png)

---

## 📂 Structure du dépôt

─lab_VLAN_Router-on-a-Stick
    │   README.md
    │
    ├───capture
    │   ├───Empty
    │   │       PC0_Ping_Fail.png
    │   │
    │   ├───Solution
    │   │       PC0_Ping.png
    │   │       R0_show_run.png
    │   │       SW0_show_vlan_trunk.png
    │   │
    │   └───Topology
    │           Topology.png
    │
    ├───configs
    │       R0.txt
    │       SW0.txt
    │       SW1.txt
    │
    └───pkt
            cisco_routage_inter_vlans_completed.pkt
            cisco_routage_inter_vlans_empty.pkt


---

## ⚡ Configurations clés

### SW0
```text
vlan 10
name bleu
vlan 20
name jaune
vlan 30
name rouge

interface fa0/1
 switchport mode access
 switchport access vlan 10
interface fa0/2
 switchport mode access
 switchport access vlan 10
interface fa0/3
 switchport mode access
 switchport access vlan 20
interface fa0/4
 switchport mode access
 switchport access vlan 20

interface fa0/5
 switchport mode trunk
 switchport trunk allowed vlan 10,20,30
interface fa0/6
 switchport mode trunk
 switchport trunk allowed vlan 10,20,30
SW1
text
Copier le code
interface fa0/1
 switchport mode access
 switchport access vlan 10
interface fa0/2
 switchport mode access
 switchport access vlan 20
interface fa0/3
 switchport mode access
 switchport access vlan 30

interface fa0/5
 switchport mode trunk
 switchport trunk allowed vlan 10,20,30
R1
text
Copier le code
interface fa0/0.10
 encapsulation dot1q 10
 ip address 192.168.10.254 255.255.255.0

interface fa0/0.20
 encapsulation dot1q 20
 ip address 192.168.20.254 255.255.255.0

interface fa0/0.30
 encapsulation dot1q 30
 ip address 192.168.30.254 255.255.255.0
✅ Tests à effectuer
Ping inter-VLAN depuis un PC vers les gateways et autres VLANs

Vérification des VLANs sur les switches :
show vlan brief

Vérification des trunks :
show interface trunk

📂 Fichiers Packet Tracer
cisco_routage_inter_vlans_empty.pkt – topologie “Empty” avant configuration

cisco_routage_inter_vlans_completed.pkt – topologie finale avec configuration complète

📸 Captures d’écran
Empty : captures avant configuration (ping échoué)

Solution : captures après configuration (ping réussi, show vlan, show trunk)

Topology : images de la topologie (vide ou complète)

💬 Objectifs pédagogiques
Comprendre la séparation des VLANs et le rôle du trunk

Apprendre la configuration Router-on-a-Stick

Développer la capacité à tester et vérifier la connectivité inter-VLAN
