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

Architecture orientée services avec API centralisée.

## Modules fonctionnels

- Gestion des projets techniques
- Rôles utilisateurs (RG, Lumière, Son, Plateau)
- Parc matériel
- État opérationnel du matériel
- Déclaration d’incidents
- Historique technique par date
- Support temps réel

## Stack technique

- Node.js
- PostgreSQL
- API REST
- Application mobile cross-platform
- Architecture modulaire

## Installation globale (dev)

1. Cloner tous les repositories StageOps
2. Configurer les variables d’environnement
3. Lancer l’API
4. Lancer l’application mobile
5. (optionnel) Lancer le gateway IoT

## Organisation du projet

Ce repository sert de point d’entrée et de documentation globale du système.
