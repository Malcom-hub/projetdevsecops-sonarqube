# Analyse SonarQube - Projet DevSecOps

## 1. Résultats

L’analyse de l’application Node.js avec SonarQube donne les résultats suivants :

- Bugs : 0  
- Vulnerabilities : 0  
- Security Hotspots : 2  
- Code Smells : 0  
- Quality Gate : PASSED  
- Security Rating : A  
- Maintainability : A  

---

## 2. Analyse des Security Hotspots

Deux Security Hotspots ont été identifiés.

### Hotspot 1 : Code Injection (eval)

L’utilisation de la fonction `eval()` permet l’exécution de code dynamique.  
Cette pratique est dangereuse car elle peut être exploitée pour exécuter du code malveillant.

Risque :
- Remote Code Execution (RCE)
- Injection de code

Statut :
- Acknowledged (problème identifié mais non corrigé)

---

### Hotspot 2 : Weak Cryptography

Un second hotspot concerne l’utilisation potentielle d’une cryptographie faible.

 Risque :
- sécurité insuffisante des données
- exposition à des attaques

Statut :
- Acknowledged

---

## 3. Interprétation des résultats

SonarQube n’a détecté aucune vulnérabilité critique ni bug dans l’application.

Cependant, la présence de Security Hotspots montre qu’il existe des zones sensibles nécessitant une validation humaine.

---

## 4. Limites de SonarQube

Malgré des résultats positifs, d’autres outils comme Semgrep et CodeQL ont détecté plusieurs vulnérabilités.

Cela montre que SonarQube peut ne pas détecter certaines failles critiques, notamment liées à l’exécution dynamique de code.

---

## 5. Conclusion

SonarQube est un outil efficace pour l’analyse globale de la qualité du code et une première détection des problèmes de sécurité.

Cependant, il doit être utilisé en complément d’autres outils SAST pour assurer une couverture de sécurité complète.