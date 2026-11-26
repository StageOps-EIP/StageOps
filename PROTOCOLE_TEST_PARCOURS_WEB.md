# Protocole de test des parcours Web

Ce guide prépare les essais externes de [l'issue #41](https://github.com/StageOps-EIP/StageOps/issues/41). Il sert à observer ce qu'une personne du spectacle comprend et réussit seule dans StageOps. Sa publication ne constitue pas un test réalisé.

## Préparer chaque session

- Recruter une personne extérieure à l'équipe qui prépare, exploite ou suit techniquement un spectacle. Noter sa fonction et son expérience dans le suivi privé, sans publier ses coordonnées.
- Prévoir 20 à 25 minutes. Utiliser une version navigable stable et noter son lien ou son commit. Vérifier l'accès au scénario de démonstration avant l'arrivée de la personne.
- Préparer un compte de test si l'accès l'exige ; ne jamais demander au participant son mot de passe personnel. Utiliser uniquement des données fictives et remettre le scénario à zéro entre deux sessions.
- Pour la tâche mobile, choisir un matériel fictif sans incident actif et noter son nom dans la fiche d'observation. Vérifier que le téléphone peut ouvrir la même version.
- Demander l'accord pour prendre des notes. Un enregistrement ou une citation attribuée exige un accord distinct. La personne peut s'arrêter à tout moment.

## Introduction à lire

> Nous testons l'interface, pas vos compétences. Dites à voix haute ce que vous cherchez et ce que vous pensez trouver. Je vais vous donner trois situations de travail. Je n'expliquerai pas les boutons pendant les tâches ; si vous êtes bloqué, dites-le et nous passerons à la suite. Puis-je noter vos observations de façon anonyme ?

Le modérateur donne l'objectif, puis se tait. Il ne montre ni la navigation ni le chemin attendu. Si une aide devient nécessaire, il note précisément la question et l'indice donné.

## Tâches à donner dans cet ordre

| Tâche | Consigne à lire | Réussite observable |
| --- | --- | --- |
| 1. Urgence et matériel | « Une panne importante demande votre attention. Trouvez le signalement à traiter en priorité, puis le matériel concerné. Montrez où vous suivriez son état. » | La personne choisit un incident actif prioritaire, ouvre son détail et retrouve le bon matériel. |
| 2. Signalement sur téléphone | « Vous constatez un nouveau problème sur **[matériel fictif préparé]**. Signalez-le avec une courte description, puis retrouvez votre signalement après avoir quitté l'écran. » | Le matériel est lié au nouvel incident ; le signalement est retrouvable sans indice après navigation. |
| 3. Contexte et conservation | « Dites-moi à quel spectacle et à quelle période correspondent ces informations. Ouvrez son programme. Que pensez-vous retrouver si vous rechargez la page ou changez d'appareil ? » | La personne repère que le programme initial est un exemple, trouve le conducteur et décrit correctement la conservation annoncée par l'interface. |

Ne pas corriger les réponses pendant les tâches. Si une action crée une donnée dans le scénario, vérifier la valeur réellement visible avant de noter « réussi ». La troisième tâche mesure la compréhension : noter la réponse exacte avant toute explication.

## Observer sans interpréter à la place du participant

Pour chaque tâche, relever : résultat **seul / avec aide / non terminé**, temps approximatif, chemin emprunté, hésitations, erreurs, retours en arrière et mots utilisés pour décrire l'écran. Distinguer un défaut de l'interface d'un problème de chargement ou d'accès. Demander ensuite :

1. « À quel moment avez-vous hésité ? »
2. « Qu'attendiez-vous après cette action ? »
3. « Qu'est-ce qui vous manquerait pour utiliser ce parcours dans votre travail ? »

Éviter les questions orientées comme « Le bouton était-il clair ? ». Ne pas présenter une préférence personnelle comme un retour du participant.

## Fiche d'observation privée

Conserver une fiche par session dans le suivi privé :

- Code anonyme du participant ; métier ; niveau d'expérience ; canal de recrutement ; accord pour les notes et, séparément, pour toute citation.
- Version testée (lien et commit), appareil, largeur d'écran si connue, conditions d'accès et données fictives utilisées.
- Pour chacune des trois tâches : résultat, durée approximative, chemin, hésitations, aide donnée, erreur éventuelle, propos exacts si la personne a accepté leur conservation.
- Fin de session : difficultés classées par impact sur la tâche, hypothèses à vérifier, prochain contact éventuel.

Les coordonnées, réponses individuelles et accords restent dans le suivi privé. Le wiki public peut contenir seulement des nombres vérifiés, des observations anonymisées et des liens vers des issues publiques. Une invitation, une réponse, un entretien et un test terminé sont quatre états différents.

## Transformer les résultats en décisions

Après plusieurs sessions, regrouper les difficultés récurrentes. Pour chaque problème retenu, créer ou compléter une issue avec le parcours, le comportement observé, son impact, la version testée et un critère de correction. Ne marquer [#41](https://github.com/StageOps-EIP/StageOps/issues/41) terminé qu'après de vrais essais documentés. Rejouer les mêmes tâches après correction pour comparer les résultats sans changer les critères de réussite.
