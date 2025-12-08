# CCNA Lab – Routage Inter-VLAN avec Router-on-a-Stick

## 🚀 Objectif

Ce lab permet de pratiquer le **routage inter-VLAN** avec un routeur en **Router-on-a-Stick**.  
On apprend à :  
- Créer des VLANs sur des switches  
- Configurer les ports **access** et **trunks**  
- Configurer les subinterfaces du routeur avec **encapsulation dot1q**  
- Vérifier la connectivité inter-VLAN

---

## 💡 Topologie

- **Switches** : SW0, SW1  
- **Routeur** : R1  
- **VLANs** :  
  - VLAN10 (Bleu) – 192.168.10.0/24  
  - VLAN20 (Jaune) – 192.168.20.0/24  
  - VLAN30 (Rouge) – 192.168.30.0/24  
- PCs et serveur assignés aux VLANs correspondants  


![Topo](https://github.com/saidou-dia/LabPacketTracer_Principal/blob/main/Lab_ROAS/lab_VLAN_Router-on-a-Stick/capture/Topology/Topology.png) 


## ✅ Tests à effectuer

- Ping inter-VLAN depuis un PC vers les autres VLANs  
- Vérification VLANs et trunks sur les switches :  
  - `show vlan brief`  
  - `show interface trunk`

---

## 📸 Captures recommandées

- **Topologie complète** (`topo_completed.png`)  
- **Ping réussi** depuis un PC (`PC0_ping.png`)  
- **Verification VLANs et trunks** (`show_vlan.png`, `show_trunk.png`)  


