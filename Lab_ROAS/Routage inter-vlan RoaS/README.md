Routage inter-vlan RoaS – Router-on-a-Stick (ROAS) Project

Ce projet présente la mise en place complète d’une infrastructure réseau basée sur VLAN, trunks, routage inter-VLAN (ROAS) et services DHCP, réalisée sous Cisco Packet Tracer.

Il inclut la configuration de 1 routeur, 9 switches, 2 access points, 1 serveur, ainsi que plusieurs PCs répartis par VLAN.

🚀 Objectifs du projet

Segmentation du réseau via VLANs (101/102/103/104/150/160/200)

Configuration des trunks entre switches

Déploiement du routage inter-VLAN sur un routeur (Router-on-a-Stick)

Mise en place d’un serveur DHCP (VLAN 200)

Activation du DHCP relay avec ip helper-address

Connexion de 2 points d’accès WiFi sur le VLAN 160

Tests de connectivité entre tous les VLANs

Supervision via SSH (Switches + Routeur)

🧱 Architecture

1 Routeur : R0

9 Switches : SW9 → SW17

1 Serveur VLAN 200 (DHCP)

Des PC pour chaque VLAN utilisateur

2 Access Points pour VLAN 160 (WiFi)

📁 Arborescence du projet
Network-VLAN-Management/
├── configs/          # Configurations complètes des switches + routeur
│   ├── SW9.txt
│   ├── SW10.txt
│   ├── SW11.txt
│   ├── SW12.txt
│   ├── SW13.txt
│   ├── SW14.txt
│   ├── SW15.txt
│   ├── SW16.txt
│   ├── SW17.txt
│   ├── R0.txt
│   └── VLANs.txt
│
├── pkt/              # Fichiers Packet Tracer
│   ├── Network_Topology_completed.pkt
│   └── Network_Topology_empty.pkt
│
└── capture/          # Captures d’écran pour la documentation
    ├── Topology/
    │   ├── Topology_empty.png
    │   └── Topology_completed.png
    │
    ├── Solution/
    │   ├── R0_Show_run.png
    │   ├── SW9_Show_run.png
    │   ├── SW10_Show_run.png
    │   ├── SW11_Show_run.png
    │   ├── SW12_Show_run.png
    │   ├── SW13_Show_run.png
    │   ├── SW14_Show_run.png
    │   ├── SW15_Show_run.png
    │   ├── SW16_Show_run.png
    │   ├── SW17_Show_run.png
    │   └── PC_Ping.png
    │
    └── Empty/
        └── Ping_Fail.png

🔧 Technologies et compétences utilisées

VLAN / Trunking (802.1Q)

Router-on-a-Stick

DHCP Server & DHCP Relay

Switching L2

Architecture réseau hiérarchique

SSH & management sécurisé

Troubleshooting (ping, tracert, spanning-tree, interfaces trunk…)

📡 Tests réalisés

Vérification du trunking :
show interfaces trunk sur SW15, SW16, SW17

Vérification des VLAN actifs :
show vlan brief

Vérification connectivité inter-VLAN :
ping entre PC de chaque VLAN

Accès au serveur DHCP depuis chaque VLAN

Tests de connectivité WiFi via AP (VLAN 160)

📜 Résultat

✔️ Routage inter-VLAN fonctionnel
✔️ DHPC relay opérationnel pour tous les VLANs
✔️ Communication OK entre tous les équipements
✔️ Infrastructure proprement documentée et reproductible
