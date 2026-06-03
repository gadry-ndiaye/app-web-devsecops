# Automatisation des tests de sécurité dans la chaine CI/CD 
# (Continious integration / Continuous deployment) 

## Description

Ce projet a été réalisé dans le cadre de mon Mastère 1 Cybersécurité et Cloud Computing.

L'objectif est de mettre en œuvre une chaîne CI/CD sécurisée intégrant des contrôles de sécurité automatisés selon l'approche DevSecOps.

# Architecture DevSecOps
Le pipeline repose sur les composants suivants :

* GitHub : gestion du code source
* Jenkins : intégration continue et automatisation
* Docker : conteneurisation de l'application
* SonarQube : analyse statique du code (SAST)
* Trivy : analyse des vulnérabilités et des images Docker
* OWASP ZAP : tests de sécurité dynamiques (DAST)

## Pipeline DevSecOps

1. Développeur pousse le code vers GitHub
2. Jenkins déclenche automatiquement le pipeline
3. Construction de l'application Docker
4. Analyse statique avec SonarQube
5. Analyse des vulnérabilités avec Trivy
6. Déploiement de l'environnement de test
7. Scan dynamique avec OWASP ZAP
8. Génération des rapports de sécurité
9. Validation avant mise en production

## Outils utilisés

* Git / GitHub
* Jenkins
* Docker
* SonarQube
* Trivy
* OWASP ZAP
* Ubuntu Linux

## Compétences mises en œuvre

* DevSecOps
* CI/CD
* Analyse de vulnérabilités
* SAST
* DAST
* Sécurité des conteneurs
* Automatisation des contrôles de sécurité
# Captures du projet
![Architecture](Screenshot%202026-06-03%20013702.png)
## Jenkins
![Jenkins](Screenshot%202026-06-03%20014532.png)
## Jenkins Pipeline
![Jenkins Pipeline](Screenshot%202026-06-03%20015252.png)
Cette capture présente le pipeline Jenkins WebGoat-DevSecOps avec l'historique des builds, les stages d'exécution et l'intégration des contrôles de sécurité.
## Analyse SonarQube
![SonarQube](Screenshot%202026-06-03%20020223.png)
![Trivy](Screenshot%202026-06-03%20020302.png)
![OWASP ZAP](Screenshot%202026-06-03%20020331.png)
## Analyse des dépendances avec Trivy (SCA)

Trivy a été utilisé pour analyser les dépendances de l'application et détecter les vulnérabilités connues (CVE).

### Résumé du scan

### Détail des vulnérabilités détectées

![Trivy Vulnerabilities](Screenshot%202026-06-03%20021232.png)
## Tests de sécurité dynamiques avec OWASP ZAP (DAST)

OWASP ZAP a été intégré au pipeline DevSecOps afin d'effectuer des tests de sécurité dynamiques sur l'application déployée. Cette étape permet d'identifier les vulnérabilités exploitables avant la mise en production.

### Résultats du scan DAST

![OWASP ZAP Scan](Screenshot%202026-06-03%20022316.png)

Cette analyse présente les vulnérabilités détectées par OWASP ZAP ainsi que leur niveau de criticité.

### Détail des alertes de sécurité

![OWASP ZAP Alerts](Screenshot%202026-06-03%20022341.png)
Les alertes générées permettent d'identifier les faiblesses de sécurité potentielles et de mettre en œuvre les mesures correctives nécessaires avant le déploiement.
![OWASP ZAP Scan](Screenshot%202026-06-03%20023121.png)
![OWASP ZAP Alerts](Screenshot%202026-06-03%20023203.png)

Les résultats obtenus démontrent l’intérêt de cette approche. L’analyse réalisée avec SonarQube a permis d’identifier 35 
bugs, 8 vulnérabilités, 69 Security Hotspots et 455 Code Smells, tout en validant le projet grâce à un Quality Gate Passed. 
Les scans effectués avec Trivy ont révélé 292 vulnérabilités sur l’environnement analysé, dont 2 critiques, 35 élevées, 100 
moyennes et 139 faibles, ainsi que 74 vulnérabilités supplémentaires dans les dépendances Maven et plusieurs secrets JWT 
exposés dans le code source. De son côté, OWASP ZAP a détecté 8 alertes de sécurité, notamment l’absence de jetons Anti
CSRF, des en-têtes HTTP de sécurité manquants et des configurations de cookies insuffisamment sécurisées. 
## Auteur

Abdoul Gadry Ndiaye

Mastère Cybersécurité et Cloud Computing
