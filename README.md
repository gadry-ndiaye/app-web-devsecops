# DevSecOps CI/CD Security Automation

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
## Auteur

Abdoul Gadry Ndiaye

Mastère Cybersécurité et Cloud Computing
