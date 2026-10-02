# StageOps

Plateforme de gestion technique pour régisseurs de spectacle vivant.

StageOps centralise la gestion du matériel, des incidents, des rôles techniques et des projets scéniques en temps réel.  
Le système est conçu pour fonctionner dans des environnements à faible budget où un seul régisseur peut superviser plusieurs pôles techniques.

## Vision

Remplacer les fichiers Excel, les notes papier et les outils dispersés par une plateforme unifiée adaptée aux contraintes du spectacle vivant.

## Architecture globale

StageOps est composé de plusieurs services indépendants :

- StageOps-Api → backend métier
- StageOps-mobile-app → interface utilisateur
- StageOps-iot-gateway → collecte d’état matériel
- StageOps-BenchMark → tests de performance

Architecture orientée services avec API centralisée et interfaces Web et Mobile.

## Modules fonctionnels

- Gestion des projets techniques
- Rôles utilisateurs (RG, Lumière, Son, Plateau)
- Parc matériel
- État opérationnel du matériel
- Déclaration d’incidents
- Historique technique par date
- Support temps réel

## Stack technique

- Backend Go / Fiber
- CouchDB et stratégie offline-first
- API REST
- Web React / Vite / React Three Fiber
- Mobile React Native
- Architecture polyrepo modulaire

## Installation globale (dev)

1. Cloner tous les repositories StageOps
2. Configurer les variables d’environnement
3. Lancer l’API
4. Lancer l’application mobile
5. (optionnel) Lancer le gateway IoT

## Organisation du projet

Ce repository sert de point d’entrée et de documentation globale du système.

- [Méthodologie de travail et utilisation du GitHub Project](METHODOLOGIE_PROJET.md)
- [GitHub Project StageOps](https://github.com/orgs/StageOps-EIP/projects/2)
- [Wiki produit et technique](https://github.com/StageOps-EIP/StageOps/wiki)
- [Répartition des responsabilités](https://github.com/StageOps-EIP/StageOps/wiki/R%C3%A9partition-des-t%C3%A2ches)

Toute fonctionnalité doit être reliée à une issue, un milestone, une modification de code et une page Wiki avant d’être considérée comme terminée.
