# Plan des objectifs complémentaires — StageOps

Ce document formalise les deux objectifs complémentaires retenus pour StageOps et la manière de les réaliser, de les mesurer et de les présenter au jury.

## Pourquoi ce plan existe

Le plan sert à transformer deux objectifs EIP assez larges en travail concret pour l'équipe : tâches, responsables, échéances, preuves et critères de réussite. Il permet aussi d'éviter deux pièges : contacter des acteurs sans aboutir à une collaboration réelle, ou recueillir des avis sans modifier le produit.

## Les deux objectifs retenus

### 1. Établir des partenariats stratégiques

StageOps est un outil métier destiné au spectacle vivant. Pour être crédible, le projet doit être confronté à un acteur réel du secteur : théâtre, salle de concert, festival, association culturelle, école ou prestataire technique.

Ce choix apporte trois bénéfices :

- un accès à des situations et contraintes réelles ;
- une validation métier au-delà de l'équipe étudiante ;
- un terrain pour tester StageOps et obtenir des preuves concrètes.

**Résultat minimum visé :** une collaboration formalisée, un test ou mini-pilote réalisé et un témoignage exploitable.

### 2. Optimiser la relation avec le public cible

StageOps doit être construit avec ses futurs utilisateurs : régisseurs, techniciens son, lumière et plateau, responsables de lieux et organisateurs d'événements.

Ce choix permet de relier chaque évolution importante à un besoin observé sur le terrain. Il rend aussi les arbitrages plus simples : l'équipe développe ce qui résout les problèmes les plus fréquents ou les plus bloquants.

**Résultat minimum visé :** deux cycles de retours avec des personnes extérieures au groupe et au moins deux évolutions du produit justifiées par ces retours.

## Principe de fonctionnement

Les deux objectifs sont traités comme une seule boucle :

1. un partenaire donne accès au terrain et à des utilisateurs pertinents ;
2. l'équipe observe leurs pratiques et recueille leurs retours ;
3. les retours sont triés et transformés en décisions produit ;
4. les évolutions sont développées et documentées ;
5. les mêmes utilisateurs retestent le produit ;
6. les résultats deviennent des preuves pour le jury et des apprentissages pour la suite.

## Plan d'exécution sur huit semaines

| Période | Partenariats | Relation utilisateurs | Livrables attendus |
| --- | --- | --- | --- |
| Semaine 1 | Sélectionner 2 à 3 profils de partenaires prioritaires | Définir les profils d'utilisateurs à interroger | Carte des partenaires, critères de sélection, guide d'entretien |
| Semaine 2 | Préparer la proposition de valeur et les messages de contact | Préparer formulaire, entretien et scénario de test | Kit de contact, formulaire, protocole de test |
| Semaine 3 | Contacter au moins 5 structures et obtenir des rendez-vous | Mener les premiers entretiens exploratoires | Traces des contacts, comptes rendus, verbatims |
| Semaine 4 | Cadrer un mini-pilote avec la structure la plus engagée | Réaliser une première session de test sur StageOps | Accord écrit, captures, problèmes observés |
| Semaine 5 | Faire valider le périmètre et les critères du pilote | Regrouper, prioriser et relier les retours aux issues | Synthèse des retours, décisions, issues GitHub |
| Semaines 6 et 7 | Maintenir le suivi avec le partenaire | Développer au moins deux améliorations prioritaires | Pull requests, documentation Wiki, avant/après |
| Semaine 8 | Présenter le résultat du pilote et demander un témoignage | Faire retester les améliorations et mesurer leur effet | Résultats, second feedback, témoignage, dossier de preuves |

## Répartition proposée pour une équipe de six

| Rôle | Responsabilité principale |
| --- | --- |
| Référent partenariat | Prospection, rendez-vous, accord et suivi du partenaire |
| Référent utilisateur / UX | Entretiens, tests, synthèse des retours et priorisation |
| Référent produit / Project | User stories, critères d'acceptation, milestones et décisions |
| Référent web | Évolutions concrètes et démontrables de l'interface Web |
| Référent backend / données | API, modèle de données, traçabilité et fiabilité du pilote |
| Référent mobile / QA / documentation | Tests, cohérence multiplateforme, Wiki et dossier de preuves |

Chaque tâche reste collective : un référent est responsable du suivi, mais la réalisation peut impliquer plusieurs membres.

## Utilisation du GitHub Project

Créer deux epics ou deux ensembles d'issues identifiables :

- `OBJ-1 — Partenariats stratégiques` ;
- `OBJ-2 — Relation avec le public cible`.

Chaque issue doit contenir :

- une user story ou un résultat attendu ;
- un responsable et, si nécessaire, des contributeurs ;
- un milestone ;
- des critères d'acceptation vérifiables ;
- un lien vers la preuve ou la page Wiki correspondante.

Les statuts suivent la méthode définie dans `METHODOLOGIE_PROJET.md`. Une tâche n'est terminée que si le résultat et sa preuve sont documentés.

## Indicateurs de réussite

### Partenariats

- 5 structures ciblées et contactées de manière personnalisée ;
- 2 rendez-vous métier obtenus ;
- 1 collaboration ou mini-pilote formalisé par écrit ;
- 1 résultat concret : test terrain, données, recommandation ou intégration ;
- 1 témoignage du partenaire.

### Relation utilisateurs

- 6 à 10 utilisateurs externes rencontrés ou testeurs ;
- 2 cycles distincts de retours ;
- une synthèse qualitative et quantitative ;
- au moins 2 évolutions produit reliées à des retours récurrents ;
- un comparatif avant/après et un second test de validation.

## Preuves à conserver pour le jury

- carte des partenaires et critères de choix ;
- messages ou courriels de prise de contact ;
- accord ou confirmation écrite du pilote ;
- formulaires, guides d'entretien et protocoles de test ;
- verbatims anonymisés et synthèse des retours ;
- issues GitHub et décisions associées ;
- captures avant/après des évolutions ;
- liens vers les pull requests et les pages Wiki ;
- résultats du second test ;
- témoignage du partenaire ou d'un utilisateur.

## Déroulé de présentation conseillé

1. rappeler le problème : les équipes techniques utilisent encore des outils dispersés et peu adaptés au terrain ;
2. expliquer pourquoi StageOps a besoin d'un partenaire métier et d'une boucle de retours utilisateurs ;
3. présenter le plan en huit semaines ;
4. montrer les indicateurs et la répartition dans l'équipe ;
5. conclure sur les preuves attendues : une collaboration réelle et deux évolutions du produit directement reliées au terrain.

## Phrase de conclusion

> Notre objectif n'est pas seulement d'affirmer que StageOps répond au terrain : nous voulons le démontrer par un partenaire engagé, des retours externes documentés et des évolutions produit que l'on peut relier à ces retours.

## Référence

Ce plan applique les critères du document **G-EIP-600 — Track Solution**, notamment les sections consacrées à *Establish Strategic Partnerships* et *Optimizing Relationships with the Target Audience*.
