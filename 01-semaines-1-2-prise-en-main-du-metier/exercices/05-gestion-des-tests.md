# Exercice 05 — Gestion des activités de test (Exercise 05 — Managing the Test Activities)

## Objectif (Objective)

Appliquer les notions de planification des tests (_test planning_), de gestion des risques (_risk management_), de suivi, de contrôle et d’achèvement des tests (_test monitoring, control and completion_), de gestion de configuration (_configuration management_) et de gestion des défauts (_defect management_).

## Mise en situation (Scenario)

Une équipe prépare une nouvelle version d’une boutique en ligne pour la fin de la semaine. Cette version modifie le paiement par carte, le calcul des frais de livraison et l’affichage de la confirmation de commande. Le paiement par carte est un parcours essentiel pour les ventes. La page d’aide, moins consultée, a aussi été mise à jour.

La livraison est prévue vendredi. Les tests doivent commencer demain, mais l’environnement de test a été indisponible une journée. La version candidate est identifiée, et l’équipe dispose d’un environnement de test, de données de paiement fictives et de trois personnes pour tester. Une personne connaît bien le paiement ; les deux autres connaissent surtout les parcours de commande.

À la veille de la livraison, le bilan provisoire est le suivant :

- 40 tests sont prévus, 25 sont exécutés, 19 réussis, 4 échoués et 2 bloqués ;
- les tests de paiement couvrent les paiements acceptés, mais pas encore les refus ni les interruptions de connexion ;
- un défaut ouvert empêche certains clients de terminer leur paiement ;
- un défaut mineur modifie l’alignement d’un titre sur la page d’aide ;
- la correction du paiement doit être retestée, puis les zones concernées par la modification doivent être vérifiées pour les régressions.

Une autre équipe prendra en charge la maintenance après la livraison. Elle a besoin de savoir quelle version et quelle configuration ont été testées, ainsi que les défauts et les risques encore ouverts.

## Travail demandé (Tasks)

### 1. Préparer un plan de test (Prepare a Test Plan)

À partir du scénario, propose les éléments principaux d’un plan de test :

- les objectifs et le périmètre des tests ;
- les éléments inclus et un élément pouvant être testé avec une priorité moindre ;
- l’approche, les niveaux et types de test pertinents ;
- les responsabilités et les ressources nécessaires ;
- les environnements, données et dépendances ;
- un critère d’entrée et deux critères de sortie ;
- une estimation simple de la capacité ou du temps disponible, en indiquant tes hypothèses.

### 2. Analyser et prioriser les risques (Analyze and Prioritize Risks)

Identifie au moins :

- deux risques produit, en estimant leur probabilité, leur impact et leur priorité ;
- un risque projet et une action pour le réduire ;
- les tests à réaliser en premier et la justification de cet ordre.

Utilise une échelle simple (par exemple faible, moyen, élevé) et explique brièvement tes choix.

### 3. Suivre et contrôler les tests (Monitor and Control Testing)

- Interprète les chiffres du bilan provisoire sans conclure uniquement à partir du nombre de tests réussis.
- Indique quelles informations supplémentaires seraient nécessaires pour évaluer l’avancement et la qualité.
- Propose au moins deux actions de contrôle face aux tests échoués ou bloqués et à l’environnement indisponible.
- Explique comment l’équipe devrait réévaluer le calendrier ou la décision de livraison.

### 4. Définir l’achèvement des tests (Define Test Completion)

- Propose des critères permettant de décider si les tests de cette version peuvent être achevés.
- Indique quelles informations doivent figurer dans le bilan final.
- Explique comment documenter et communiquer les défauts ouverts et les risques résiduels.
- Cite les éléments de test utiles à archiver ou à transférer à l’équipe de maintenance.

### 5. Assurer la gestion de configuration (Apply Configuration Management)

Liste les éléments de configuration qu’il faut identifier ou conserver afin de savoir précisément ce qui a été testé et de pouvoir reproduire les résultats. Inclue la version candidate, l’environnement et les données de test.

### 6. Rédiger un rapport de défaut (Write a Defect Report)

Rédige un rapport concis pour le défaut qui empêche certains clients de terminer le paiement. N’invente pas les informations manquantes : note les questions ou les éléments qu’il faudrait obtenir.

Le rapport doit aider une autre personne à comprendre et reproduire le problème, et distinguer la sévérité du défaut de sa priorité de traitement.

### 7. Prévoir le retest et la régression (Plan Retesting and Regression Testing)

Après la correction du défaut de paiement :

- propose un retest pour confirmer que le défaut est corrigé ;
- propose deux tests de régression liés aux zones potentiellement affectées ;
- indique les conditions nécessaires pour que les résultats soient interprétables.

## Réponse à compléter (Answer Template)

### Plan de test (Test Plan)

- Objectifs :
- Périmètre inclus :
- Hors périmètre ou priorité moindre :
- Approche et activités de test :
- Responsabilités :
- Environnement et données :
- Dépendances et contraintes :
- Critère d’entrée :
- Critères de sortie :
- Estimation et hypothèses :

### Analyse des risques (Risk Analysis)

| Risque | Produit ou projet ? | Probabilité | Impact | Priorité | Action ou tests proposés |
| ------ | ------------------- | ----------- | ------ | -------- | ------------------------ |
|        |                     |             |        |          |                          |
|        |                     |             |        |          |                          |
|        |                     |             |        |          |                          |

Ordre de priorité des tests et justification :

### Suivi et contrôle (Monitoring and Control)

- Interprétation du bilan provisoire :
- Informations supplémentaires nécessaires :
- Action face aux tests échoués :
- Action face aux tests bloqués ou à l’environnement indisponible :
- Décision ou réévaluation du calendrier de livraison :

### Achèvement et transfert (Completion and Handover)

- Critères d’achèvement :
- Informations du bilan final :
- Défauts ouverts et risques résiduels à communiquer :
- Éléments à archiver ou transmettre :

### Configuration testée (Tested Configuration)

- Version ou identifiant de la livraison :
- Environnement et configuration :
- Données utilisées :
- Cas de test et résultats associés :
- Autres éléments à conserver :

### Rapport de défaut (Defect Report)

- Titre :
- Version et environnement :
- Préconditions et données :
- Étapes pour reproduire :
  1.
  2.
  3.
- Résultat attendu :
- Résultat observé :
- Preuves disponibles ou à recueillir :
- Sévérité et justification :
- Priorité et justification :
- Informations manquantes :

### Retest et régression (Retesting and Regression Testing)

- Retest du défaut corrigé :
- Test de régression 1 et justification :
- Test de régression 2 et justification :
- Conditions pour interpréter les résultats :

## Auto-évaluation (Self-Assessment)

Avant de considérer l’exercice terminé, vérifier que :

- le plan tient compte du périmètre, des ressources, des contraintes et des objectifs ;
- les risques produit sont distingués des risques projet et influencent réellement l’ordre des tests ;
- le suivi s’appuie sur plusieurs indicateurs, pas seulement sur le nombre de tests réussis ;
- les actions de contrôle répondent aux problèmes constatés ;
- les critères d’achèvement prennent en compte les défauts et les risques résiduels ;
- les versions, environnements et données testés sont identifiables ;
- le rapport de défaut est reproductible et distingue sévérité et priorité ;
- le retest et les tests de régression ont des objectifs différents.

_Rédige tes réponses sans consulter de corrigé. Tu peux ensuite me les envoyer pour une correction argumentée._
