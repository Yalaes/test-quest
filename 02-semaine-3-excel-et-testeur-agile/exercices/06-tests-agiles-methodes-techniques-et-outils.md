# Exercice 06 — Méthodes et techniques de test Agile

## Objectif

Préparer une approche de test pour une user story, choisir des techniques pertinentes et expliquer les retours attendus dans une équipe Agile. L’exercice ne demande pas de configurer une pipeline ni d’utiliser un outil d’automatisation spécialisé.

## Mise en situation

Une équipe développe une fonction permettant d’appliquer un code promotionnel au panier.

Règles confirmées :

- un code valide applique une réduction de 10 % une seule fois par commande ;
- un code inconnu ou expiré ne réduit pas le montant ;
- le client reçoit un message compréhensible après l’application du code.

Règles à clarifier :

- les codes sont-ils cumulables ?
- la réduction s’applique-t-elle aux frais de livraison ?
- que se passe-t-il si le panier est modifié après l’application du code ?

## Travail demandé

### 1. Préparer la collaboration sur le besoin

- Écris une question à discuter avec la personne responsable du produit pour chacune des règles à clarifier.
- Rédige un exemple d’acceptation au format **Étant donné / Quand / Alors** pour une règle confirmée.
- Indique en quoi cet exemple aide l’équipe à partager le comportement attendu.

### 2. Concevoir des tests à partir des risques

Propose au moins quatre vérifications, en utilisant au minimum deux techniques étudiées en semaine 01-02 :

- classes d’équivalence ou valeurs limites ;
- table de décision ;
- transitions d’état ;
- test exploratoire ou devin des erreurs.

Pour chaque vérification, indique le risque ou le comportement visé, les données nécessaires et le résultat attendu.

### 3. Organiser les retours dans l’itération

- À quel moment l’équipe peut-elle relire les critères et préparer les exemples ?
- Comment tester la fonctionnalité dès qu’un incrément est disponible ?
- Quel retour communiquer au reste de l’équipe si un critère est ambigu ou un défaut bloque la suite ?
- Quels tests de régression pourraient être utiles après une modification du calcul du panier ?

### 4. Situer TDD, ATDD, BDD et CI

Complète le tableau avec l’objectif principal et les participants concernés. Ne confonds pas la pratique avec l’outil qui pourrait la soutenir.

| Approche | Objectif principal | Participants / moment |
| --- | --- | --- |
| TDD | | |
| ATDD | | |
| BDD | | |
| Intégration continue | | |

Explique pourquoi la CI ne remplace pas les revues, l’exploration et l’analyse humaine des résultats.

## Réponse à compléter

### Questions sur les règles ouvertes

1.
2.
3.

### Exemple d’acceptation

Étant donné …
Quand …
Alors …

### Conception des vérifications

| Test | Technique choisie | Risque / comportement visé | Données et résultat attendu |
| --- | --- | --- | --- |
| | | | |
| | | | |
| | | | |
| | | | |

### Retours et régression

- Moment de clarification :
- Retour lorsque le critère est ambigu :
- Retour lorsqu’un défaut bloque :
- Tests de régression proposés :

### Approches Agile et CI

| Approche | Objectif principal | Participants / moment |
| --- | --- | --- |
| TDD | | |
| ATDD | | |
| BDD | | |
| CI | | |

Pourquoi la CI ne remplace-t-elle pas les activités humaines ?

## Auto-évaluation

- Les règles ouvertes restent des questions et ne sont pas transformées en suppositions.
- Les tests couvrent des comportements positifs, négatifs et des risques pertinents.
- Les techniques choisies sont nommées et adaptées aux règles.
- Les tests et retours sont prévus pendant l’itération.
- TDD, ATDD, BDD et CI sont distingués selon leur objectif.
- L’exercice reste au niveau des méthodes et techniques Agile, sans anticiper les modules d’outils spécialisés.
