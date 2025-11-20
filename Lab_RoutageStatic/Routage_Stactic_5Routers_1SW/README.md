# Lab Routage Statique – 5 Routeurs et 1 Switch

## 🎯 Objectif
Ce lab a pour but de configurer un réseau avec **routage statique** sur 5 routeurs et 1 switch, et de vérifier la connectivité entre les PC à travers le réseau. Il permet de pratiquer :  

- Configuration des interfaces et IP  
- Routage statique  
- Tests de connectivité (ping, tracert)  
- Analyse des captures de réussite et d’échec  

---

## 🌐 Topologie
La topologie complète est disponible dans la capture :  
`captures/solution/topology_complete.png`  

> Les routeurs R0 à R4 sont configurés sur des **sous-réseaux distincts** pour éviter les conflits IP.

---

## ⚙️ Configurations
Toutes les configurations de routeurs R0 à R4 sont visibles via les captures `show running-config` dans :  
`captures/solution/`

---

## 📡 Tests de connectivité
- **Ping réussi et tracert OK** → captures dans `captures/solution/`  
- **Ping échoué et tracert négatif** → captures dans `captures/empty/`  

> Chaque capture illustre soit la réussite, soit l’échec de la connectivité pour un apprentissage complet.

---

## ✅ Conclusion
Ce lab permet de :  

- Comprendre le fonctionnement du **routage statique**  
- Identifier et résoudre les problèmes de connectivité  
- Travailler avec des **sous-réseaux distincts** pour éviter les conflits IP  
- Préparer des rapports et captures pédagogiques pour GitHub
