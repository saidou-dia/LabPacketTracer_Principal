# Lab Troubleshooting – Exercice 2

##  Objectif
Identifier et corriger les erreurs de configuration empêchant la communication entre PC0 et PC1 à travers les routeurs R0 à R4.

---

##  Contenu du dossier

### **1. pkt/**
- `Exo2 vierge.pkt` → topologie initiale non corrigée  
- `exo2 corrige.pkt` → topologie corrigée et fonctionnelle  

### **2. captures/**

#### Vierge
Contient l’état initial des équipements et tests échoués :  
- `R0_show_run.png`  
- `R1_show_run.png`  
- `R2_show_run.png`  
- `R3_show_run.png`  
- `R4_show_run.png`  
- `PC0_ipconfig.png`  
- `PC1_ipconfig.png`  
- `ping_FAIL.png`  
- `PC0_traceroute_PC1_FAIL.png`  *(bloque au routeur R2)*  
- `PC1_traceroute_PC0_FAIL.png`  *(bloque au routeur R3)*  

#### Solution
Contient les configurations finales et tests réussis :  
- `R0_show_run.png`  
- `R1_show_run.png`  
- `R2_show_run.png`  
- `R3_show_run.png`  
- `R4_show_run.png`  
- `ping_Tracert_OK.png`  

#### Topologies
- `topologie_vierge.png`  
- `topologie_solution.png`  

---

##  Approche de Troubleshooting

1. **Analyse de la topologie**
   - Identifier les liens entre R0 → R4 et les PC.  
   - Vérifier les sous-réseaux, IP et interfaces de chaque équipement.  

2. **Tests initiaux de connectivité**
   - Ping PC0 → PC1 (échoue)  
   - Ping PC1 → PC0 (échoue)  
   - Traceroute PC0 → PC1 (bloque au routeur R2)  
   - Traceroute PC1 → PC0 (bloque au routeur R3)  

3. **Vérification des configurations**
   - `show running-config` sur R0 à R4  
   - Vérifier :  
     - Adresses IP et masques des interfaces  
     - Interfaces administratives activées (`no shutdown`)  
     - Routes statiques ou dynamiques correctes  
     - Passerelles par défaut  

4. **Identification des erreurs**
   - Routes manquantes ou incorrectes  
   - Interfaces shutdown  
   - Masques de sous-réseau incorrects  
   - Mauvaise passerelle par défaut  

5. **Correction**
   - Ajouter ou corriger les routes statiques  
   - Activer les interfaces shutdown  
   - Corriger les adresses IP et masques  
   - Vérifier la propagation des routes si protocole dynamique utilisé  

6. **Validation finale**
   - Ping PC0 ↔ PC1 (réussi)  
   - Traceroute complet PC0 ↔ PC1 (réussi)  
   - Vérification des tables de routage des routeurs  

7. **Conclusion**
   - La connectivité complète entre PC0 et PC1 est rétablie.  
   - Tous les tests sont fonctionnels et les configurations finales documentées.

---

##  Notes
- Les captures “vierge” montrent **où ça bloque** pour le troubleshooting (R2 et R3).  
- Les captures “solution” montrent **la configuration correcte et les tests réussis**.  
- Cette approche permet de **comparer facilement avant / après** et de documenter la résolution.

