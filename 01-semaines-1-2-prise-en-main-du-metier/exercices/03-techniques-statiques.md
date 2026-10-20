# Exercice 03 — Techniques statiques (Exercise 03 — Static Testing)

## Objectif (Objective)

Appliquer les notions de test statique (_static testing_), de test dynamique (_dynamic testing_), de revue (_review_), de processus et de rôles de revue, ainsi que d’analyse statique (_static analysis_).

## Mise en situation (Scenario)

Une équipe développe une fonction de remboursement pour une boutique en ligne. Avant le développement, elle partage les éléments suivants pour relecture :

> **Exigence A** : « Le remboursement doit être traité rapidement après la demande du client. »
>
> **Exigence B** : « Le client peut demander un remboursement dans les 30 jours suivant l’achat. Les achats réalisés pendant une promotion ne sont pas remboursables. »
>
> **Critère d’acceptation** : « Un client peut demander le remboursement d’un achat promotionnel dans les 30 jours suivant l’achat. »

Une personne de l’équipe propose une revue technique. L’auteur présente les exigences en réunion, mais les participants ne les ont pas reçues à l’avance. Une seule personne prend des notes ; aucun critère de revue ni suivi des anomalies n’a été prévu.

Après le développement, un outil d’analyse statique signale les éléments suivants :

1. Une variable est déclarée mais jamais utilisée.
2. Une branche de code semble inaccessible.
3. Une fonction reçoit directement une valeur fournie par l’utilisateur sans validation détectée par la règle de sécurité de l’outil.

## Travail demandé (Tasks)

### 1. Distinguer test statique et dynamique (Distinguish Static and Dynamic Testing)

Pour chacune des activités suivantes, indique s’il s’agit d’un test statique ou dynamique et justifie ta réponse :

- relire l’exigence A avant le développement ;
- utiliser un outil pour examiner le code source sans le lancer ;
- exécuter un scénario de remboursement avec un compte de test ;
- examiner la documentation utilisateur avant sa publication.

Explique aussi pourquoi les activités statiques ne rendent pas les tests dynamiques inutiles.

### 2. Relever les problèmes dans les exigences (Review the Requirements)

- Repère au moins deux problèmes, ambiguïtés ou contradictions dans les exigences et le critère d’acceptation.
- Pour chaque problème, explique le risque ou la question qu’il soulève.
- Propose une question à poser à la personne responsable du besoin pour clarifier chaque point.
- Réécris l’exigence A de manière plus précise, en indiquant toute hypothèse nécessaire plutôt que d’inventer une règle métier.

### 3. Améliorer la revue (Improve the Review)

- Identifie au moins trois faiblesses dans la revue proposée.
- Propose une amélioration pour chacune, en t’appuyant sur le processus de revue.
- Indique quels rôles seraient utiles et décris brièvement leur responsabilité : auteur, responsable de revue, facilitateur, réviseur et scribe.
- Parmi les quatre types suivants, lequel correspond le mieux à la revue prévue ? Justifie ta réponse : revue informelle (_informal review_), walkthrough (_walkthrough_), revue technique (_technical review_) ou inspection (_inspection_).

### 4. Analyser les alertes de l’outil (Analyze the Tool Findings)

Pour chacune des trois alertes de l’outil :

- explique ce qu’elle peut indiquer ;
- précise si elle confirme à elle seule un défaut ;
- indique quelle vérification ou action de suivi serait pertinente.

Distingue notamment une alerte potentiellement non pertinente d’un défaut confirmé après analyse.

### 5. Choisir les techniques adaptées (Choose Appropriate Techniques)

Pour chacun des éléments ci-dessous, propose une technique statique appropriée et indique ce qu’elle pourrait détecter :

- une exigence qui utilise le terme « rapidement » ;
- un code source contenant une branche potentiellement inaccessible ;
- une documentation dont une étape ne correspond plus au fonctionnement prévu.

Indique ensuite un test dynamique qui resterait utile pour vérifier le comportement de remboursement à l’exécution.

## Réponse à compléter (Answer Template)

### Statique ou dynamique (Static or Dynamic)

| Activité (Activity) | Type de test (Test type) | Justification (Reason) |
| ------------------- | ----------------------- | ---------------------- |
|                     |                         |                        |
|                     |                         |                        |
|                     |                         |                        |
|                     |                         |                        |

Pourquoi les tests statiques ne remplacent-ils pas les tests dynamiques ?

### Revue des exigences (Requirements Review)

| Problème repéré (Finding) | Risque ou question (Risk or Question) | Question de clarification (Clarifying Question) |
| ------------------------- | ------------------------------------- | ------------------------------------------------ |
|                           |                                       |                                                  |
|                           |                                       |                                                  |

Réécriture de l’exigence A :

### Revue (Review)

- Faiblesse 1 et amélioration proposée :
- Faiblesse 2 et amélioration proposée :
- Faiblesse 3 et amélioration proposée :
- Type de revue choisi et justification :

| Rôle (Role) | Responsabilité pendant cette revue (Responsibility) |
| ----------- | ----------------------------------------------------- |
| Auteur      |                                                     |
| Responsable de revue |                                            |
| Facilitateur |                                                    |
| Réviseur    |                                                     |
| Scribe      |                                                     |

### Alertes d’analyse statique (Static Analysis Findings)

| Alerte (Finding) | Ce qu’elle peut indiquer | Confirme-t-elle un défaut ? | Vérification ou suivi |
| ---------------- | ------------------------ | -------------------------- | --------------------- |
| Variable inutilisée |                      |                            |                       |
| Branche inaccessible |                    |                            |                       |
| Valeur utilisateur non validée |           |                            |                       |

### Techniques adaptées (Appropriate Techniques)

| Élément à examiner (Work Product) | Technique statique proposée | Problème recherché |
| --------------------------------- | --------------------------- | ------------------ |
| Exigence ambiguë                  |                             |                    |
| Code source                       |                             |                    |
| Documentation utilisateur         |                             |                    |

Test dynamique à effectuer :

## Auto-évaluation (Self-Assessment)

Avant de considérer l’exercice terminé, vérifier que :

- les activités statiques sont distinguées des activités qui exécutent le logiciel ;
- les problèmes relevés dans les exigences sont formulés sans inventer de règles métier ;
- les améliorations proposées correspondent à des étapes concrètes du processus de revue ;
- les rôles de revue sont distingués selon leurs responsabilités ;
- les alertes de l’outil sont analysées et ne sont pas automatiquement traitées comme des défauts confirmés ;
- un test dynamique complémentaire est proposé.

_Rédige tes réponses sans consulter de corrigé. Tu peux ensuite me les envoyer pour une correction argumentée._
