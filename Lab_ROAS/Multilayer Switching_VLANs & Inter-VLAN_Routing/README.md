Réseau d’Entreprise – Multilayer Switching & Routage Inter-VLAN

Ce projet présente la mise en place complète d’une infrastructure réseau d’entreprise basée sur la segmentation VLAN, le trunking 802.1Q et le routage inter-VLAN assuré par un switch multilayer (Layer 3), réalisée sous Cisco Packet Tracer.

Il inclut la configuration d’un routeur WAN, d’un switch cœur L3, de plusieurs switches d’accès, de points d’accès WiFi, d’un serveur et de postes clients répartis par VLAN.

---

🚀 Objectifs du projet

- Segmentation du réseau via VLANs (101 / 102 / 103 / 104 / 150 / 160 / 200)
- Mise en place d’une architecture hiérarchique (Core / Access)
- Configuration des trunks entre le switch multilayer et les switches d’accès
- Routage inter-VLAN via SVI sur switch Layer 3
- Déploiement d’un serveur DHCP dans le VLAN 200
- Activation du DHCP relay avec `ip helper-address`
- Connexion de points d’accès WiFi sur le VLAN 160
- Mise en place d’un VLAN de management (VLAN 150)
- Tests complets de connectivité inter-VLAN et WiFi
- Connexion WAN via routeur edge

---

🧱 Architecture

- 1 Routeur (WAN / Edge)
- 1 Switch Multilayer Cisco 3560 (Core Layer 3)
- 6 Switches d’accès Cisco 2960
- 1 Serveur (VLAN 200 – DHCP)
- Plusieurs PCs répartis par VLAN utilisateur
- 2 Access Points (VLAN 160 – WiFi)

---

🔧 Technologies et compétences utilisées

- VLAN & Trunking (802.1Q)
- Switching Layer 2
- Switching Layer 3 & routage inter-VLAN
- SVI (Switch Virtual Interfaces)
- DHCP Server & DHCP Relay
- Architecture réseau hiérarchique
- Management réseau (VLAN Management)
- Dépannage réseau (ping, traceroute, show vlan, show interfaces trunk)

---

📡 Tests réalisés

- Vérification du trunking :
  - `show interfaces trunk` sur le switch multilayer et les switches d’accès
- Vérification des VLANs actifs :
  - `show vlan brief`
- Vérification des SVI et du routage :
  - `show ip route`
- Tests de connectivité inter-VLAN :
  - `ping` entre postes de VLANs différents
- Attribution DHCP pour chaque VLAN
- Tests de connectivité WiFi via les Access Points (VLAN 160)
- Test de connectivité vers le routeur WAN

---

📜 Résultats

✔️ Routage inter-VLAN pleinement fonctionnel  
✔️ DHCP relay opérationnel pour tous les VLANs  
✔️ Accès WiFi segmenté et fonctionnel  
✔️ Communication OK entre tous les équipements  
✔️ Infrastructure proprement documentée et reproductible  

---

📂 Contenu du repository

- Configurations complètes du routeur, du switch multilayer et des switches d’accès
- Fichier Packet Tracer du lab
- Documentation claire pour reproduction ou évolution du projet

---

📘 Contexte

Projet réalisé dans un objectif de montée en compétences sur les architectures réseau Cisco, la segmentation VLAN et le routage inter-VLAN en environnement d’entreprise.

