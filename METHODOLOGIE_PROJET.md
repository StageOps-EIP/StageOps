# Méthodologie de travail StageOps

Ce document est la règle commune de l’équipe StageOps. Il explique comment transformer un besoin terrain en fonctionnalité démontrable, comment utiliser le GitHub Project et comment conserver une documentation exploitable pendant toute la durée de l’EIP.

## 1. Sources de vérité

| Besoin | Source de vérité |
| --- | --- |
| Vision, roadmap et avancement transversal | [GitHub Project StageOps](https://github.com/orgs/StageOps-EIP/projects/2) |
| Travail à réaliser et critères d’acceptation | Issues du dépôt [StageOps](https://github.com/StageOps-EIP/StageOps/issues) |
| Code et décisions d’implémentation | Dépôt technique concerné et pull request |
| Fonctionnement durable d’une feature | [Wiki StageOps](https://github.com/StageOps-EIP/StageOps/wiki) |
| Preuves de tests, benchmarks et soutenance | Wiki, lié depuis l’issue |

Une information ne doit pas être dupliquée avec des versions contradictoires. Le Project agrège le travail ; l’issue décrit le résultat attendu ; le Wiki explique le résultat livré.

## 2. Organisation du GitHub Project

### 2.1 Statuts du workflow

| Statut | Signification | Condition d’entrée | Condition de sortie |
| --- | --- | --- | --- |
| `Backlog` | Besoin identifié, pas encore prêt | Valeur utilisateur comprise | Definition of Ready satisfaite |
| `Ready` | Travail suffisamment détaillé pour démarrer | User story, critères, responsable, domaine, priorité, estimation et milestone renseignés | Un membre commence réellement le travail |
| `In progress` | Implémentation ou étude active | Branche créée et propriétaire actif | Pull request prête ou blocage identifié |
| `In review` | Relecture technique et validation fonctionnelle | Pull request ouverte, tests passés, documentation Wiki préparée | Revue acceptée et démonstration validée |
| `Blocked` | Impossible d’avancer sans dépendance ou décision | Motif, responsable du déblocage et prochaine date de contrôle commentés | Dépendance levée |
| `Done` | Valeur livrée et traçable | Definition of Done entièrement satisfaite | Aucun retour en arrière ; une régression crée un bug séparé |

Le statut décrit l’avancement uniquement. Le domaine technique ne doit jamais être utilisé comme statut.

### 2.2 Champs obligatoires

Chaque item doit avoir les champs suivants avant de passer en `Ready` :

- `Assignees` : un responsable principal, éventuellement un binôme ;
- `Status` : état réel du workflow ;
- `Priority` : `P0`, `P1` ou `P2` ;
- `Estimate` : charge en jours idéaux (`0.5`, `1`, `1.5`, `2`, puis découpage obligatoire au-delà) ;
- `Size` : `XS`, `S`, `M` ou `L` pour la lecture de roadmap ;
- `module` : domaine métier (`Core`, `Permission`, `Lumière`, `Son`, `Plateau`, `3D`, `Offline`, `Export`) ;
- `Type de travail` : `Caractéristique`, `Bug`, `Dette technique`, `Étude` ou `Documentation` ;
- `Domaine` : `Backend`, `Web`, `Mobile`, `DevOps`, `QA/Sécurité` ou `Documentation` ;
- `Milestone` : un et un seul jalon de livraison.

### 2.3 Priorités

- `P0` : indispensable au prochain parcours de démonstration ou bloque une autre équipe ;
- `P1` : nécessaire au milestone courant, mais contournement temporaire possible ;
- `P2` : amélioration utile qui ne bloque ni la démo ni l’intégration.

Une priorité n’est pas une préférence personnelle. Toute modification de priorité doit être justifiée dans l’issue.

### 2.4 Vues à utiliser

- **Backlog** : raffinage, champs manquants et ordre global ;
- **Priority board** : pilotage hebdomadaire par statut et priorité ;
- **Team items** : charge des six membres et détection des personnes bloquées ;
- **Roadmap** : cohérence entre issues et milestones ;
- **My items** : travail quotidien individuel.

## 3. Milestones StageOps

Les jalons représentent des résultats démontrables, pas seulement des dates.

1. **Réalignement et dette documentaire** : dépôts, stack réelle, lancement, méthode et documentation cohérents.
2. **MVP intégré** : authentification, projets, rôles, matériel et incidents utilisables de bout en bout.
3. **Parité Web/Mobile et mode hors-ligne** : mêmes règles métier, scénarios hors connexion et synchronisation vérifiés.
4. **Exports, temps réel et RUL** : exports métier, événements temps réel et suivi de durée de vie.
5. **Qualité, démonstration et livrables RNCP** : tests terrain, sécurité, accessibilité, scénario de démo et preuves EIP.

Règles :

- chaque milestone possède une description, une date cible validée en équipe et un critère de sortie mesurable ;
- chaque issue appartient à un seul milestone ;
- une issue non terminée n’est pas déplacée silencieusement : le report est expliqué dans un commentaire ;
- la revue du milestone se termine par une démonstration et un court status update du Project.

## 4. Écrire une user story exploitable

### 4.1 Format du titre

`[Domaine] Verbe + résultat utilisateur`

Exemple : `[Web] Déclarer un incident et le retrouver après rechargement`.

### 4.2 Corps d’issue

```md
## User story
En tant que régisseur général,
je veux déclarer un incident lié à un équipement,
afin que toute l’équipe voie immédiatement le problème et son état.

## Valeur métier
Évite la perte d’information entre le plateau, la régie et le changement d’équipe.

## Critères d’acceptation
- [ ] Les champs obligatoires sont validés.
- [ ] L’incident apparaît dans le registre.
- [ ] Le compteur du dashboard est mis à jour.
- [ ] L’incident reste présent après rechargement.
- [ ] Le parcours clavier et le mode sombre sont vérifiés.

## Hors périmètre
- Synchronisation distante si l’API n’est pas encore intégrée.

## Dépendances
- Issue ou endpoint concerné, avec lien.

## Plan de démonstration
1. État initial.
2. Action utilisateur.
3. Résultat visible.
4. Rechargement ou cas d’erreur.

## Preuves attendues
- Pull request ou commit.
- Tests exécutés.
- Page Wiki de la feature.
- Capture ou vidéo courte si l’interface change.
```

Une story Web et une story Mobile peuvent partager le même besoin métier, mais elles doivent être des sous-issues d’une story parent ou porter clairement leur domaine. Les doublons sans relation sont interdits.

## 5. Definition of Ready

Une issue peut passer en `Ready` uniquement si :

- la user story et sa valeur métier sont compréhensibles par un non-développeur ;
- les critères d’acceptation sont testables ;
- le périmètre et le hors-périmètre sont écrits ;
- les dépendances sont identifiées ;
- le domaine, le module, le type, la priorité, l’estimation, le responsable et le milestone sont renseignés ;
- le parcours de démonstration attendu est décrit ;
- la charge ne dépasse pas deux jours idéaux, sinon la story est découpée.

## 6. Cycle de développement

1. Sélectionner une issue `Ready` du milestone courant.
2. La passer en `In progress` au moment où le travail commence.
3. Créer une branche `feature/<issue>-<slug>`, `fix/<issue>-<slug>` ou `docs/<issue>-<slug>`.
4. Utiliser des commits lisibles : `feat(web): ...`, `fix(api): ...`, `docs(wiki): ...`.
5. Relier la pull request à l’issue avec `Refs #N` ; utiliser `Closes #N` seulement si toute la Definition of Done est satisfaite.
6. Exécuter les tests et documenter les résultats dans la pull request.
7. Créer ou mettre à jour la page Wiki de la feature avant `In review`.
8. Faire relire par au moins un membre qui n’est pas l’auteur.
9. Démontrer le parcours fonctionnel.
10. Fusionner, vérifier `main`, puis passer l’item en `Done`.

Les correctifs directs sur `main` sont réservés à une urgence de démonstration. Ils doivent ensuite être reliés à une issue et documentés comme les autres changements.

## 7. Definition of Done

Une feature est `Done` lorsque :

- tous les critères d’acceptation sont cochés et réellement vérifiés ;
- le build, le lint et les tests du dépôt concerné passent ;
- les erreurs et états vides importants sont traités ;
- l’accessibilité clavier et le responsive sont contrôlés pour une interface ;
- la pull request ou le commit est lié à l’issue ;
- la page Wiki existe et contient la preuve de validation ;
- le scénario de démonstration est reproductible depuis un état initial connu ;
- aucune dépendance critique n’est masquée ;
- le changement est disponible sur `main`.

## 8. Documentation obligatoire d’une feature dans le Wiki

Nom de page : `Feature - <domaine> - <nom court>`.

Chaque page doit contenir :

```md
# Feature — Domaine — Nom

## Problème utilisateur
## User story et issue liée
## Périmètre livré / non livré
## Parcours utilisateur
## Règles métier
## Architecture et données
## API et dépendances
## États d’erreur et limites connues
## Accessibilité, sécurité et hors-ligne
## Tests et preuves
## Procédure de démonstration
## Historique des décisions
```

La page doit relier l’issue du dépôt `StageOps`, le dépôt technique, la pull request ou le commit, et le milestone. Une capture seule ne remplace pas l’explication.

## 9. Rituels de l’équipe de six personnes

### Début de semaine — 30 minutes

- revoir le milestone actif ;
- vérifier la Definition of Ready des prochains items ;
- limiter chaque personne à une tâche principale `In progress` ;
- confirmer les dépendances entre Backend, Web, Mobile, DevOps et QA.

### Point asynchrone — deux fois par semaine

Chaque membre écrit : `fait / prochain / blocage / preuve` dans l’issue active. Un blocage de plus de 24 heures passe en `Blocked`.

### Fin de semaine — 45 minutes

- démonstration des parcours terminés ;
- revue du Project et des milestones ;
- contrôle des pages Wiki ;
- publication d’un status update court : réalisé, risques, décisions, prochaines actions.

## 10. Règles de démonstration

Une feature présentée doit avoir un parcours de 60 à 120 secondes :

1. annoncer le problème métier ;
2. montrer l’état initial ;
3. effectuer une seule action principale ;
4. montrer l’effet dans au moins un autre écran si pertinent ;
5. recharger pour prouver la persistance ou montrer le fonctionnement hors ligne ;
6. réinitialiser les données de démonstration.

Le présentateur dispose d’un compte ou mode de démonstration connu, d’un jeu de données stable et d’une solution de repli par capture/vidéo.

## 11. Mesures suivies

- nombre d’items `Ready`, `In progress`, `Blocked` et `Done` par milestone ;
- temps moyen entre `In progress` et `Done` ;
- couverture des features par une page Wiki ;
- nombre de tests utilisateurs et retours transformés en décisions ;
- dette connue : bugs ouverts, documentation manquante, bundle ou performance hors budget.

La méthode évolue par décision d’équipe. Toute modification importante est expliquée dans une issue de documentation et résumée dans le Wiki.
