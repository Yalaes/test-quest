# Exercice 04 — Techniques de conception des tests (Exercise 04 — Test Techniques)

## Objectif (Objective)

Appliquer les techniques boîte noire (_black-box testing_), boîte blanche (_white-box testing_), basées sur l’expérience (_experience-based testing_) et les approches collaboratives (_collaboration-based test approaches_).

## Mise en situation (Scenario)

Une boutique en ligne propose une livraison standard gratuite pour les commandes d’au moins 50 euros. En dessous de ce montant, la livraison standard coûte 5 euros. Les commandes d’au moins 100 euros peuvent aussi bénéficier d’une réduction fidélité de 10 %, si le client est membre du programme. Les règles ne précisent pas si le montant utilisé pour déterminer la livraison est calculé avant ou après la réduction fidélité.

Le compte client est verrouillé après trois tentatives de connexion échouées. Une connexion réussie remet le compteur d’échecs à zéro.

Le développeur partage également le pseudo-code suivant pour calculer les frais de livraison :

```text
fraisLivraison = 5
si montantCommande >= 50
    fraisLivraison = 0
afficher fraisLivraison
```

L’équipe souhaite clarifier les règles avec les parties prenantes et concevoir des tests avant la prochaine livraison.

## Travail demandé (Tasks)

### 1. Partitionner les entrées (Partition the Inputs)

Pour le montant de commande :

- définis les classes d’équivalence valides et invalides pertinentes ;
- propose une valeur représentative pour chaque classe ;
- justifie pourquoi ces valeurs devraient être traitées de la même façon.

Tu peux préciser les hypothèses nécessaires si les règles ne définissent pas de montant minimum ou maximum.

### 2. Tester les valeurs limites (Test Boundary Values)

- Identifie les limites métier pour les frais de livraison et la réduction fidélité.
- Pour chaque limite, propose les valeurs juste en dessous, sur la limite et juste au-dessus.
- Indique le résultat attendu lorsque celui-ci est déterminé par le scénario.
- Note la question à clarifier sur le montant utilisé pour appliquer les règles combinées.

### 3. Construire une table de décision (Build a Decision Table)

Construis une table de décision pour les frais de livraison et la réduction fidélité, avec au minimum les conditions suivantes :

- montant de commande inférieur à 50 euros, ou au moins égal à 50 euros ;
- montant de commande inférieur à 100 euros, ou au moins égal à 100 euros ;
- client membre ou non membre.

Indique pour chaque combinaison le coût de livraison et la réduction attendus, ou marque le résultat comme « à clarifier » lorsque les règles ne permettent pas de conclure. Évite de conserver des combinaisons impossibles ou redondantes sans les justifier.

### 4. Modéliser les transitions d’état (Model State Transitions)

Décris les états possibles du compte et les événements qui provoquent un changement d’état. Propose une séquence de tests qui vérifie :

- les deux premières tentatives échouées ;
- le verrouillage à la troisième tentative échouée ;
- le comportement d’une tentative supplémentaire lorsque le compte est verrouillé ;
- la remise à zéro du compteur après une connexion réussie.

Précise les préconditions et le résultat attendu pour chaque étape.

### 5. Vérifier la structure du code (Use White-box Testing)

À partir du pseudo-code fourni :

- indique les branches possibles ;
- propose un test permettant d’exécuter toutes les instructions ;
- propose le nombre minimal de tests nécessaires pour parcourir les deux branches ;
- donne une valeur d’entrée pour chaque test et le résultat attendu ;
- compare la couverture des instructions obtenue avec le premier test à la couverture des branches ;

Explique enfin pourquoi une couverture de branches complète ne prouve pas à elle seule l’absence de défauts.

### 6. Utiliser l’expérience et explorer (Use Experience and Explore)

Propose :

- trois cas de test issus du devin des erreurs (_error guessing_) pour le panier ou la connexion ;
- une charte courte de test exploratoire (_exploratory testing_) indiquant un objectif, un périmètre et une durée ;
- une liste de contrôle de trois points à réutiliser pour vérifier le calcul de commande.

### 7. Clarifier le besoin en collaboration (Collaborate on the Requirements)

- Formule deux questions que l’équipe devrait discuter avec les parties prenantes avant de finaliser les tests.
- Rédige un exemple d’acceptation en format **Étant donné / Quand / Alors** (_Given / When / Then_) pour une règle clairement déterminée par le scénario.
- Vérifie que le résultat attendu est observable par le client et n’introduit pas de règle métier non fournie.

## Réponse à compléter (Answer Template)

### Classes d’équivalence (Equivalence Classes)

| Classe | Valide ou invalide ? | Valeur représentative | Résultat attendu / justification |
| ------ | ------------------- | --------------------- | -------------------------------- |
|        |                     |                       |                                  |
|        |                     |                       |                                  |
|        |                     |                       |                                  |

### Valeurs limites (Boundary Values)

| Limite | Valeur juste en dessous | Valeur sur la limite | Valeur juste au-dessus | Résultats attendus |
| ------ | ----------------------- | ------------------- | ---------------------- | ------------------ |
| 50 euros |                       |                     |                        |                    |
| 100 euros |                      |                     |                        |                    |

Question à clarifier sur les règles combinées :

### Table de décision (Decision Table)

| Montant < 50 ? | Montant >= 100 ? | Client membre ? | Frais de livraison | Réduction fidélité |
| -------------- | ---------------- | --------------- | ------------------ | ------------------ |
|                |                  |                 |                    |                    |
|                |                  |                 |                    |                    |
|                |                  |                 |                    |                    |
|                |                  |                 |                    |                    |

Combinaisons impossibles ou redondantes à retirer ou à expliquer :

### Transitions d’état (State Transitions)

- États du compte :
- Événements :
- Règle de verrouillage :

| Étape | État initial / précondition | Événement | État ou résultat attendu |
| ----- | --------------------------- | --------- | ------------------------ |
|       |                             |           |                          |
|       |                             |           |                          |
|       |                             |           |                          |
|       |                             |           |                          |

### Couverture boîte blanche (White-box Coverage)

- Branche 1 et test associé :
- Branche 2 et test associé :
- Test qui exécute toutes les instructions :
- Nombre minimal de tests pour couvrir toutes les branches :
- Différence de couverture obtenue :
- Pourquoi la couverture complète ne prouve-t-elle pas l’absence de défauts ?

### Techniques basées sur l’expérience (Experience-based Techniques)

- Cas issus du devin des erreurs :
  1.
  2.
  3.
- Charte exploratoire :
  - Objectif :
  - Périmètre :
  - Durée :
- Liste de contrôle :
  1.
  2.
  3.

### Approche collaborative (Collaborative Approach)

- Questions à discuter :
  1.
  2.
- Exemple d’acceptation :

```gherkin
Étant donné ...
Quand ...
Alors ...
```

## Auto-évaluation (Self-Assessment)

Avant de considérer l’exercice terminé, vérifier que :

- les classes d’équivalence et les valeurs limites correspondent aux règles données ;
- les combinaisons de la table de décision sont cohérentes et les ambiguïtés sont signalées ;
- les séquences de transitions précisent les états et les résultats attendus ;
- les tests boîte blanche parcourent les deux issues de la décision ;
- les tests basés sur l’expérience sont concrets et liés aux risques du scénario ;
- l’exemple d’acceptation est compréhensible, observable et ne suppose pas une règle non spécifiée.

_Rédige tes réponses sans consulter de corrigé. Tu peux ensuite me les envoyer pour une correction argumentée._
