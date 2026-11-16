# Plan d'action — Track Solution

Ce plan transforme le retour de mentorat du 11 novembre 2026 en résultats vérifiables. Le [GitHub Project](https://github.com/orgs/StageOps-EIP/projects/2) reste la source de vérité pour les responsables, les statuts et les échéances. Les quatre objectifs ci-dessous doivent chacun avoir un responsable nommé par l'équipe. Une tâche sans responsable reste en `Backlog`.

## État de départ

- Les développements Web, 3D, mobile et backend progressent, mais les preuves d'usage externe sont encore insuffisantes.
- Les comptes Instagram et Facebook ont été annoncés par l'équipe. Leur pertinence pour les professionnels ciblés reste à démontrer.
- La refonte visuelle et les maquettes existent ; aucun test utilisateur externe documenté n'est encore établi dans le retour de mentorat.
- Aucune collaboration formalisée ni reconnaissance externe vérifiable n'est encore établie dans ce retour.
- Le déploiement backend partagé dépend de l'obtention d'un VPS.

Ces constats sont un point de départ, pas des statuts `Done`. Une preuve ultérieure doit être reliée à l'issue correspondante.

## Responsabilités à confirmer

| Objectif | Responsable à désigner | Livrable principal | Preuve de sortie |
| --- | --- | --- | --- |
| Obligatoire 1 — Communauté et bêta-testeurs | À désigner | Analyse des canaux, registre de contacts, recrutement de 20 bêta-testeurs qualifiés et actifs | Sources des canaux, historique des contacts, consentement et participation effective aux tests |
| Obligatoire 2 — UX/UI | À désigner | Parcours prioritaire, protocole de test, journal V0 → V3 | Observations externes, décisions reliées aux versions et comparatif des résultats |
| Complémentaire A — Partenariats | À désigner | Cartographie de structures, propositions de collaboration, pilote | Échanges datés, accord ou engagement explicite et résultat du pilote |
| Complémentaire C — Crédibilité et reconnaissance | À désigner | Avis ou relais provenant d'acteurs extérieurs | Témoignage attribuable, publication tierce ou autre trace vérifiable |

Le responsable coordonne le résultat et les preuves ; les contributions peuvent être partagées entre Web, mobile, backend et communication. L'équipe doit confirmer les quatre noms et une date de revue avant de passer les issues en `Ready`.

## Issues à créer dans le Project

Chaque issue doit être ajoutée au Project, associée au jalon **5 — Qualité, démonstration et livrables RNCP**, et garder le statut `Backlog` jusqu'à ce que les champs de la [Definition of Ready](METHODOLOGIE_PROJET.md#5-definition-of-ready) soient remplis. Les titres et critères ci-dessous sont prêts à copier dans GitHub.

### O1.1 — `[Solution] Comparer les canaux où se trouvent les professionnels du spectacle`

- Rechercher Instagram, Facebook et LinkedIn avec les mêmes critères : présence de régisseurs, responsables techniques, salles, prestataires et organisateurs ; activité des communautés ; accès possible à un échange professionnel.
- Relever des exemples publics de groupes, pages ou structures et conserver leurs URL ainsi que la méthode de recherche.
- Conclure quel canal sert à identifier les contacts, lequel sert à publier des démonstrations et lequel ne mérite pas d'effort immédiat.
- **Terminé quand** un tableau sourcé et une décision motivée sont liés à l'issue. L'ouverture d'un compte ne suffit pas.

### O1.2 — `[Solution] Constituer et suivre une cohorte de bêta-testeurs qualifiés`

- Définir les critères d'éligibilité : métier, rôle dans la préparation d'un spectacle, possibilité de tester un parcours réel.
- Tenir un registre privé : structure, fonction, canal, date de prise de contact, réponse, prochaine action, accord pour le test et participation. Ne pas publier de coordonnées personnelles dans une issue publique.
- Préparer un message court et personnalisable ; mesurer les contacts, les réponses, les personnes recrutées et les tests effectivement réalisés.
- **Terminé quand** au moins 20 personnes qualifiées et actives ont participé et que les preuves anonymisées sont disponibles. Les simples invitations ne comptent pas.

### O2.1 — `[UX] Définir un parcours prioritaire et tester la version actuelle`

- Choisir un scénario métier complet, par exemple préparer un projet puis déclarer et retrouver un incident.
- Écrire les tâches à donner au testeur, les questions neutres, les observations à relever, le consentement et les règles d'anonymisation.
- Réaliser des tests avec des professionnels extérieurs à l'équipe ; relever réussite, erreurs, hésitations, temps et verbatims utiles.
- **Terminé quand** une synthèse des problèmes observés, classés par impact, est reliée aux issues produit correspondantes.

### O2.2 — `[UX] Documenter les itérations V0 à V3 et leurs effets`

- Conserver les maquettes ou captures de chaque version sans écraser les précédentes.
- Pour chaque changement : problème observé, source du retour, décision, modification, date de version et résultat du nouveau test.
- Comparer au moins un même parcours avant et après avec les mêmes critères de réussite.
- **Terminé quand** le journal permet de remonter de chaque évolution importante à une observation externe et à une mesure après modification. Une préférence esthétique interne n'est pas une validation utilisateur.

### A.1 — `[Solution] Cartographier les partenaires métier et préparer un pilote`

- Identifier des salles, théâtres, festivals et prestataires techniques pertinents, avec les rôles à contacter dans chaque structure.
- Distinguer expertise métier, accès à des utilisateurs, mise en relation et expérimentation sur un événement réel.
- Suivre les démarches et les réponses dans le registre privé commun, sans publier les coordonnées dans GitHub.
- **Terminé quand** une structure accepte explicitement un périmètre de collaboration, un interlocuteur et une prochaine étape ; conserver la preuve de l'accord.

### C.1 — `[Solution] Obtenir et documenter un retour professionnel externe`

- Identifier des professionnels et communautés capables de tester, commenter ou relayer StageOps.
- Demander un avis sur un usage ou un résultat concret, avec accord sur la manière de le citer ou de le partager.
- Distinguer les publications de l'équipe des avis et relais provenant d'acteurs tiers.
- **Terminé quand** au moins une manifestation d'intérêt externe attribuable est vérifiable et que son contexte est documenté. Un post publié par l'équipe ne suffit pas.

## Dépendances et points de contrôle

1. **Nom StageOps :** comparer l'acteur au nom proche, son domaine et le risque de confusion avant une communication plus large. Cette vérification ne remplace pas une analyse juridique.
2. **VPS backend :** documenter le besoin d'hébergement, le propriétaire du déblocage et la solution de démonstration temporaire.
3. **Comptes sociaux :** si une plateforme est inaccessible à une partie de l'équipe, confier la création et l'administration à un membre qui y a accès ; conserver une gouvernance claire des comptes.
4. **Supports et IA :** relier les affirmations de présentation à des issues, tests, captures ou échanges réels. L'équipe doit pouvoir expliquer et démontrer chaque résultat.

## Revue d'avancement

À chaque point d'équipe, consigner pour chaque objectif : **fait / prochaine action / blocage / responsable / preuve**. Le prochain support doit montrer les quatre objectifs séparément, avec les actions réalisées et les résultats observés, sans confondre une tâche préparée avec une validation externe obtenue.
