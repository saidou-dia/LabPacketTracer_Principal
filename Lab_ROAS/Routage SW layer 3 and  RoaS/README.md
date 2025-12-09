# Routage Inter-VLAN : Switch L3 et L2

**Serial Number** : 1983-1116

## Description

Ce projet Packet Tracer illustre la configuration d’un réseau avec routage inter-VLAN entre un **Switch L3 (3560-24PS)** et un **Switch L2 (2960-24TT)**, incluant :

- VLANs séparés pour différents groupes de PCs  
- Trunk entre Switch L3 et L2  
- Serveur DHCP/DNS sur VLAN30 pour distribution d’adresses IP  

--

## VLANs

| VLAN  | Couleur | Appareils |
|-------|---------|-----------|
| VLAN10 | Bleu    | PC0, PC1, PC2, PC4 |
| VLAN20 | Jaune   | PC2, PC3, PC5 |
| VLAN30 | Rouge   | Serveur DHCP/DNS |

---

## Connexions

- **Router**
  - Fa0/0 → Serveur DNS  
  - Fa0/1 → Switch L3 (Fa0/6)  

- **Switch L3**
  - VLAN10 → PC0, PC1, PC2  
  - VLAN20 → PC2, PC3  
  - VLAN30 → Serveur DHCP  
  - Trunk → Switch L2 (Fa0/5 ↔ Fa0/3)  

- **Switch L2**
  - VLAN10 → PC4  
  - VLAN20 → PC5  
  - VLAN30 → Serveur0  
  - Trunk → Switch L3  

---

## Notes

- La configuration `ip helper-address` est nécessaire sur les interfaces VLAN10 et VLAN20 du Switch L3 pour permettre aux PCs d’obtenir une IP depuis le serveur DHCP VLAN30.  
- La topologie est contenue dans le fichier `.pkt` fourni dans le dossier `pkt`.
