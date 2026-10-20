# Techniques de conception des tests (Test Techniques)

## Objectifs d’apprentissage (Learning Objectives)

À la fin de cette fiche, je dois pouvoir :

- expliquer à quoi servent les techniques de conception des tests ;
- appliquer des techniques boîte noire à des exemples simples ;
- distinguer les techniques boîte blanche des techniques boîte noire ;
- décrire les techniques basées sur l’expérience et les approches collaboratives ;
- choisir une technique en fonction du contexte et des informations disponibles.

## 1. Pourquoi utiliser des techniques de test ? (Why Use Test Techniques?)

Une **technique de test** (_test technique_) aide à identifier les conditions de test, les cas de test et les données à utiliser. Elle fournit une manière structurée de concevoir des tests à partir d’une base de test, de la structure du logiciel ou de l’expérience des personnes.

Une **base de test** (_test basis_) est l’information utilisée pour concevoir les tests : exigences, récits utilisateurs, règles métier, conception, code ou expérience d’utilisation du produit.

Les techniques aident à organiser la conception des tests, mais aucune technique ne garantit à elle seule l’absence de défauts. Une équipe peut en combiner plusieurs selon le produit, les risques, le temps disponible et les informations accessibles.

## 2. Techniques boîte noire (Black-box Test Techniques)

Les techniques **boîte noire** conçoivent des tests à partir du comportement attendu ou de la base de test, sans s’appuyer sur la structure interne du code.

### Partitionnement en classes d’équivalence (Equivalence Partitioning)

Le **partitionnement en classes d’équivalence** consiste à répartir les valeurs d’entrée ou les situations en groupes qui devraient être traités de la même façon. On sélectionne généralement une valeur représentative de chaque classe.

**Exemple :** un formulaire accepte les âges de 18 à 65 ans inclus.

- moins de 18 ans : classe invalide ;
- de 18 à 65 ans : classe valide ;
- plus de 65 ans : classe invalide.

Tester une valeur représentative dans chaque classe permet de couvrir les comportements attendus de ces groupes. Il faut identifier les classes à partir des règles, pas seulement choisir des valeurs au hasard.

### Analyse des valeurs limites (Boundary Value Analysis)

L’**analyse des valeurs limites** se concentre sur les limites entre les classes d’équivalence, car les erreurs sont fréquentes aux frontières.

Pour l’âge accepté de 18 à 65 ans inclus, des valeurs utiles à tester sont : **17, 18, 19, 64, 65 et 66**. Elles couvrent les valeurs juste en dessous, sur et juste au-dessus de chaque limite.

Le nombre de valeurs testées autour des limites dépend du critère de couverture choisi. Pour débuter, les trois valeurs proches de chaque limite (juste en dessous, sur la limite, juste au-dessus) rendent le raisonnement explicite.

### Test par tables de décision (Decision Table Testing)

Le **test par tables de décision** permet de tester des règles métier dont le résultat dépend de plusieurs conditions combinées. La table énumère les combinaisons pertinentes de conditions et le résultat attendu pour chacune.

**Exemple :** une commande bénéficie de la livraison gratuite si le client est membre **ou** si le montant atteint 50 euros.

| Membre ? | Montant d’au moins 50 euros ? | Livraison gratuite ? |
| --- | --- | --- |
| Non | Non | Non |
| Non | Oui | Oui |
| Oui | Non | Oui |
| Oui | Oui | Oui |

Chaque colonne de conditions représente une règle à vérifier. La table aide à repérer les combinaisons oubliées ou les résultats contradictoires.

### Test de transition d’état (State Transition Testing)

Le **test de transition d’état** s’applique lorsque le comportement du système dépend de son état actuel et des événements reçus. Un modèle d’états indique les états possibles, les transitions permises et parfois les actions ou résultats associés.

**Exemple :** après trois saisies incorrectes du code PIN, une carte est bloquée. On peut tester :

- une saisie correcte depuis l’état « actif » ;
- une saisie incorrecte et le nombre de tentatives restantes ;
- le passage à l’état « bloqué » après la troisième erreur ;
- le comportement d’une nouvelle saisie lorsque la carte est bloquée.

Cette technique peut vérifier des transitions valides, et selon le niveau de couverture choisi, des transitions invalides ou des séquences de transitions.

## 3. Techniques boîte blanche (White-box Test Techniques)

Les techniques **boîte blanche** utilisent la structure interne du logiciel, par exemple le code, les décisions ou les chemins d’exécution, pour concevoir les tests. Elles sont utiles en complément des techniques fondées sur les exigences.

### Test des instructions (Statement Testing)

Le **test des instructions** vise à exécuter les instructions exécutables du code. La couverture des instructions (_statement coverage_) mesure la proportion d’instructions exécutées par les tests.

### Test des branches (Branch Testing)

Le **test des branches** vise à parcourir les issues des décisions du code, comme les résultats vrai et faux d’une condition. La couverture des branches (_branch coverage_) mesure la proportion de branches parcourues.

La couverture des branches implique généralement la couverture des instructions, mais l’inverse n’est pas garanti. Par exemple, un test peut exécuter une instruction conditionnelle en ne prenant que son issue « vrai » : l’instruction est exécutée, mais l’issue « faux » ne l’est pas.

Les mesures de couverture indiquent ce qui a été parcouru dans le code, mais une couverture élevée ne prouve pas que les résultats attendus ont été correctement vérifiés ni que le logiciel est exempt de défauts.

## 4. Techniques basées sur l’expérience (Experience-based Test Techniques)

Ces techniques s’appuient sur les connaissances, les compétences et l’expérience des testeurs, des développeurs ou des utilisateurs. Elles sont utiles lorsque la documentation est limitée, mais leur efficacité dépend des personnes et du contexte.

### Deviner les erreurs (Error Guessing)

Le **devin des erreurs** (_error guessing_) utilise l’expérience pour anticiper les erreurs probables et concevoir des tests qui les exposent.

**Exemples :** essayer de soumettre un formulaire vide, entrer une valeur très longue, cliquer deux fois sur un bouton de paiement ou interrompre une opération en cours.

Les idées peuvent venir de défauts déjà observés, de l’usage du produit ou des erreurs fréquemment commises dans des situations similaires.

### Test exploratoire (Exploratory Testing)

Le **test exploratoire** (_exploratory testing_) consiste à apprendre le produit, concevoir des tests et les exécuter de manière étroitement liées. Les résultats d’un test orientent les prochaines explorations.

L’exploration n’est pas nécessairement improvisée : elle peut être guidée par un objectif, une charte de test, une durée et des notes sur les actions et les observations. Elle permet d’adapter les tests aux découvertes faites pendant la session.

### Test basé sur une liste de contrôle (Checklist-based Testing)

Le **test basé sur une liste de contrôle** (_checklist-based testing_) utilise des éléments de contrôle préparés pour orienter les vérifications. Une liste peut rappeler des risques, des règles ou des points à vérifier sans détailler chaque cas de test.

Une liste est rapide à réutiliser, mais elle doit être maintenue à jour. Si les testeurs la suivent mécaniquement sans analyser le contexte, des problèmes nouveaux ou spécifiques peuvent passer inaperçus.

## 5. Approches de test collaboratives (Collaboration-based Test Approaches)

Les approches collaboratives impliquent différentes parties prenantes dans la clarification du besoin et la conception des tests. Elles visent à établir une compréhension commune du comportement attendu.

### Écrire les récits utilisateurs en collaboration (Collaborative User Story Writing)

Les personnes métier, les utilisateurs, les développeurs et les testeurs peuvent contribuer ensemble à la rédaction et à la clarification d’un récit utilisateur. La discussion permet de préciser les objectifs, les limites et les critères d’acceptation avant ou pendant le développement.

### Développement piloté par les tests d’acceptation (Acceptance Test-Driven Development)

Dans le **développement piloté par les tests d’acceptation** (_Acceptance Test-Driven Development_, **ATDD**), l’équipe définit les critères ou exemples d’acceptation avant l’implémentation, avec la participation des personnes concernées. Ces exemples illustrent les résultats attendus et aident l’équipe à vérifier qu’elle partage la même compréhension du besoin.

Un format courant pour exprimer un exemple est **Étant donné / Quand / Alors** (_Given / When / Then_) :

- **Étant donné** un contexte initial ;
- **Quand** une action est réalisée ;
- **Alors** un résultat observable est attendu.

**Exemple :** Étant donné un panier d’au moins 50 euros, quand le client consulte les options de livraison, alors la livraison gratuite est proposée.

Ces exemples peuvent devenir des tests automatisés, mais l’intérêt de l’approche commence par la conversation et la clarification du besoin.

## 6. Choisir et combiner les techniques (Selecting and Combining Techniques)

Le choix d’une technique dépend notamment :

- de la base de test disponible et de sa qualité ;
- du type de comportement ou de risque à vérifier ;
- de l’accès au code et à la conception ;
- des compétences de l’équipe et du temps disponible ;
- du niveau de détail attendu pour les tests.

**Exemples de choix :**

- règles d’entrée avec des bornes numériques : partitionnement en classes d’équivalence et analyse des valeurs limites ;
- résultat dépendant de plusieurs conditions métier : table de décision ;
- parcours d’un workflow avec plusieurs états : test de transition d’état ;
- logique conditionnelle du code : test des instructions ou des branches ;
- documentation incomplète ou risques connus : test exploratoire et devin des erreurs ;
- besoin encore discuté : exemples d’acceptation conçus en collaboration.

On peut combiner les techniques. Pour un formulaire, par exemple, une table de décision peut couvrir les règles métier, l’analyse des limites les valeurs numériques, et le test exploratoire l’ergonomie du parcours.

## 7. Mise en pratique (Practical Exercise)

Une boutique applique une réduction selon la valeur du panier : aucun rabais sous 50 euros, 10 % de réduction de 50 à 99,99 euros inclus, et 15 % à partir de 100 euros. Un compte est bloqué après trois mots de passe incorrects. Le code de calcul de réduction contient aussi une décision qui distingue les paniers admissibles et non admissibles.

Pour préparer des tests :

- définis les classes d’équivalence et propose des valeurs représentatives ;
- identifie les valeurs limites pertinentes pour les deux seuils de réduction ;
- construis les colonnes principales d’une table de décision si une autre condition, telle que le statut de membre, modifie le rabais ;
- décris une séquence de test de transition d’état pour le blocage du compte ;
- explique ce que vérifieraient le test des instructions et le test des branches dans le code de calcul ;
- propose deux idées de test basées sur l’expérience.

## 8. À retenir (Key Takeaways)

- Les techniques de test structurent la conception des conditions, cas et données de test.
- Les techniques boîte noire partent du comportement attendu ; les techniques boîte blanche s’appuient sur la structure interne.
- Le partitionnement, les valeurs limites, les tables de décision et les transitions d’état couvrent différents types de règles et de comportements.
- Les techniques basées sur l’expérience mobilisent l’expertise, l’exploration et les listes de contrôle.
- Les approches collaboratives clarifient le besoin et les critères d’acceptation avec les parties prenantes.
- Les techniques peuvent être combinées ; la couverture obtenue ne prouve pas l’absence de défauts.

## 9. Pour vérifier ma compréhension (Knowledge Check)

1. Quelle différence y a-t-il entre une technique boîte noire et une technique boîte blanche ?
2. Quelle technique boîte noire convient pour des règles dépendant de plusieurs conditions ?
3. Pour un champ autorisant les nombres de 1 à 10 inclus, quelles valeurs testerais-tu autour des limites ?
4. Pourquoi le test des branches peut-il donner une couverture plus exigeante que le test des instructions ?
5. Donne une situation adaptée au test de transition d’état.
6. En quoi le test exploratoire est-il différent d’une exécution de cas de test entièrement prédéfinis ?
7. À quel moment l’approche ATDD aide-t-elle à clarifier les attentes ?
8. Une couverture de branches de 100 % prouve-t-elle l’absence de défauts ? Pourquoi ?

<details>
<summary>Correction proposée (Suggested Answers)</summary>

1. La boîte noire s’appuie sur le comportement attendu ou la base de test sans utiliser la structure interne ; la boîte blanche utilise cette structure.
2. Le test par tables de décision.
3. Pour les bornes 1 et 10 : 0, 1, 2, 9, 10 et 11, afin de vérifier juste en dessous, sur et juste au-dessus des limites.
4. Parce qu’il faut parcourir les différentes issues des décisions, alors que l’exécution d’une instruction conditionnelle ne garantit pas que toutes ses issues ont été prises.
5. Par exemple, un compte qui passe de l’état « actif » à « bloqué » après trois mots de passe incorrects.
6. En test exploratoire, l’apprentissage, la conception et l’exécution des tests se déroulent ensemble ; les observations orientent les tests suivants.
7. Avant l’implémentation, grâce à la définition collaborative de critères ou d’exemples d’acceptation qui précisent le comportement attendu.
8. Non. Elle indique que les branches ont été parcourues, mais ne garantit ni que les résultats attendus ont été correctement vérifiés ni que tous les défauts ont été trouvés.

</details>

## Références et ressources (References and Resources)

- [ISTQB — Syllabus CTFL v4.0.1](https://istqb.org/?sdm_process_download=1&download_id=3345) : chapitre 4, « Test Analysis and Design » ; voir les sections sur les techniques boîte noire (partitionnement, valeurs limites, tables de décision, transitions d’état), boîte blanche (instructions et branches), basées sur l’expérience et collaboratives.
- [Glossaire ISTQB](https://glossary.istqb.org/) : référence terminologique pour rechercher les définitions de _equivalence partitioning_, _boundary value analysis_, _decision table testing_, _state transition testing_, _statement coverage_ et _branch coverage_.
- [Cucumber — Behaviour-Driven Development](https://cucumber.io/docs/bdd/) : exemple d’outil et de pratique pour élaborer collaborativement des exemples de comportement et les relier à des tests exécutables.
- [Cucumber — Gherkin Reference](https://cucumber.io/docs/gherkin/reference/) : consulter la syntaxe des scénarios, notamment `Given`, `When`, `Then` et les tableaux d’exemples. Cette référence complète la partie pratique ; Gherkin n’est pas à lui seul une méthode complète d’ATDD.

_Cette fiche est une synthèse personnelle destinée à l’apprentissage. En cas de différence de formulation, se référer au syllabus ISTQB officiel et aux supports de formation._
