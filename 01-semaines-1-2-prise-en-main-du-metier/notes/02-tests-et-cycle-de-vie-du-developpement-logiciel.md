# Tester pendant le cycle de vie du développement logiciel (Testing Throughout the Software Development Life Cycle)

## Objectifs d’apprentissage (Learning Objectives)

À la fin de cette fiche, je dois pouvoir :

- expliquer pourquoi les tests doivent être adaptés au cycle de développement ;
- décrire comment les activités de test s’intègrent aux principaux modèles de cycle de vie ;
- distinguer les niveaux de test des types de test ;
- expliquer les approches « test en premier » et le principe du « décalage vers la gauche » ;
- reconnaître les principaux déclencheurs des tests de maintenance.

## 1. Le cycle de vie du développement logiciel (Software Development Life Cycle, SDLC)

Le **cycle de vie du développement logiciel** (_software development life cycle_, **SDLC**) désigne les activités réalisées pour concevoir, développer, livrer et maintenir un logiciel.

Selon le projet, ces activités peuvent comprendre :

- l’analyse des besoins et des exigences (_requirements analysis_) ;
- la conception de la solution ;
- le développement ;
- les tests ;
- le déploiement ;
- la maintenance et les évolutions.

Le test logiciel (_software testing_) ne constitue pas une activité isolée qui commencerait uniquement lorsque le développement est terminé. Les activités de test s’intègrent au cycle de vie choisi et peuvent commencer dès l’analyse des exigences.

**Exemple :** avant même que le code d’une règle de remboursement soit écrit, une revue peut révéler que les exigences ne précisent pas si les frais de livraison sont remboursés.

## 2. Modèles de cycle de vie et tests (Life Cycle Models and Testing)

### Modèle séquentiel (Sequential Model)

Dans un modèle séquentiel, les activités sont principalement organisées en étapes successives. Une étape est généralement terminée avant que la suivante commence.

Les tests peuvent alors être planifiés à l’avance et exécutés après certaines étapes de développement. Il reste important de vérifier les documents et les exigences plus tôt, même si l’exécution du logiciel intervient plus tard.

**Avantage :** les étapes et les livrables sont souvent définis de manière claire.

**Point de vigilance :** si les défauts ne sont recherchés qu’à la fin, ils peuvent être coûteux à corriger et retarder la livraison.

### Modèle itératif ou incrémental (Iterative or Incremental Model)

Dans un modèle itératif ou incrémental, le produit est construit et amélioré par étapes. Chaque itération ou incrément apporte des changements au produit.

Les tests ont lieu régulièrement. Les changements peuvent nécessiter des tests des nouvelles fonctionnalités ainsi que des tests de régression (_regression testing_) pour vérifier que les fonctionnalités existantes fonctionnent toujours.

**Exemple :** une première version permet de créer un compte ; une version suivante ajoute la réinitialisation du mot de passe. La nouvelle fonction est testée, et la création de compte peut être retestée pour repérer une régression.

### Approches agiles (Agile Approaches)

Les approches agiles (_Agile approaches_) privilégient des livraisons fréquentes, la collaboration et l’adaptation aux changements. Les tests sont réalisés tout au long du développement, en lien étroit avec l’équipe et les parties prenantes (_stakeholders_).

Les exigences, le développement et les tests peuvent se préciser ensemble. Cela aide l’équipe à obtenir des retours rapides et à détecter les incompréhensions plus tôt.

### Idée essentielle (Key Takeaway)

Aucun modèle ne supprime le besoin de tester. Le cycle de vie influence **quand**, **comment** et **par qui** les activités de test sont réalisées.

## 3. Bonnes pratiques applicables à différents cycles de vie (Good Practices Across Life Cycles)

Quelques pratiques sont utiles quel que soit le modèle choisi :

- associer les activités de test aux activités de développement correspondantes ;
- faire participer les testeurs et les autres parties prenantes dès que possible ;
- définir des objectifs et des critères de test (_test objectives and test criteria_) adaptés au contexte ;
- vérifier les documents et les exigences avant et pendant le développement ;
- prévoir des tests à plusieurs niveaux ;
- répéter les tests utiles après des changements, notamment les tests de régression ;
- recueillir des retours et adapter l’approche de test.

Les tests peuvent suivre une approche **dirigée par les tests** (_test-driven approach_), par exemple lorsqu’une équipe écrit d’abord des tests qui guident ensuite le développement. Cette approche est détaillée plus loin.

## 4. Les niveaux de test (Test Levels / ?Unit Tests?)

Un **niveau de test** (_test level_) représente un ensemble d’activités de test organisé autour d’un objectif et d’un périmètre particuliers. Les niveaux aident à structurer les tests, mais leur organisation exacte dépend du projet.

### Test des composants (Component Testing)

Le test des composants vérifie une partie isolée du logiciel, par exemple une fonction, une classe ou un module.

Il est souvent réalisé par les développeurs et peut être largement automatisé.

**Exemple :** vérifier qu’une fonction calcule correctement le montant d’une réduction.

### Test d’intégration (Integration Testing)

Le test d’intégration vérifie les interactions entre plusieurs composants ou systèmes.

**Exemple :** vérifier que le service de commande transmet correctement le montant au service de paiement.

### Test système (System Testing / ?E2E Tests?)

Le test système vérifie le système dans son ensemble par rapport aux exigences et aux besoins définis.

**Exemple :** vérifier le parcours complet d’achat, de la sélection d’un produit jusqu’à la confirmation de la commande.

### Test d’acceptation (Acceptance Testing)

Le test d’acceptation évalue si le système répond aux besoins et aux attentes des utilisateurs ou des autres parties prenantes. Il contribue à déterminer si le produit peut être accepté pour son usage prévu.

**Exemple :** une personne représentative des utilisateurs vérifie qu’elle peut passer une commande et retrouver son récapitulatif.

### À retenir sur les niveaux (Test Levels: Key Points)

Les niveaux se distinguent principalement par leur **périmètre** et leur **objectif**. Ils ne correspondent pas forcément chacun à une étape unique du cycle de développement.

## 5. Les types de test (Test Types)

Un **type de test** (_test type_) décrit ce qui est testé ou l’objectif du test. Différents types de test peuvent être réalisés à plusieurs niveaux.

### Tests fonctionnels (Functional Testing)

Les tests fonctionnels vérifient **ce que fait** le système : ses fonctions et ses comportements observables.

**Exemple :** vérifier qu’un utilisateur peut appliquer un code promotionnel valide.

### Tests non fonctionnels (Non-functional Testing)

Les tests non fonctionnels vérifient **comment le système fonctionne** ou certaines caractéristiques de qualité.

Ils peuvent porter, entre autres, sur :

- les tests de performance (_performance testing_) ;
- les tests d’ergonomie ou de facilité d’utilisation (_usability testing_) ;
- les tests de compatibilité (_compatibility testing_) ;
- les tests de sécurité (_security testing_) ;
- les tests de fiabilité (_reliability testing_) ;
- les tests d’accessibilité (_accessibility testing_).

**Exemple :** vérifier que la page de paiement reste réactive lorsqu’un grand nombre d’utilisateurs l’utilisent en même temps.

### Tests boîte noire et boîte blanche (Black-box and White-box Testing)

Ces termes décrivent deux façons de concevoir ou de sélectionner des tests :

- les approches **boîte noire** (_black-box testing_) s’appuient sur le comportement attendu et les spécifications, sans dépendre de la structure interne du code ;
- les approches **boîte blanche** (_white-box testing_) s’appuient sur la structure interne du logiciel, par exemple le code ou les chemins d’exécution.

Les techniques correspondantes seront étudiées dans la fiche sur les techniques de conception des tests.

### Niveaux et types : ne pas confondre (Levels and Types: Do Not Confuse Them)

Le niveau répond surtout à la question : **« quelle partie du système teste-t-on et dans quel périmètre ? »**

Le type répond plutôt à la question : **« quel comportement ou quelle caractéristique cherche-t-on à vérifier ? »**

**Exemple :** un test de performance peut être réalisé au niveau système. « Système » est le niveau ; « performance » est le type.

## 6. Approches « test en premier » (Test-first Approaches)

Dans une approche **test en premier** (_test-first approach_), les tests sont conçus ou écrits avant le code correspondant, ou en même temps que la définition du besoin. Ils aident à préciser le comportement attendu.

Quelques exemples :

- **Développement piloté par les tests** (_Test-Driven Development_, **TDD**) : les développeurs écrivent d’abord un test automatisé, puis le code nécessaire pour le réussir ;
- **Développement piloté par les tests d’acceptation** (_Acceptance Test-Driven Development_, **ATDD**) : l’équipe définit des critères ou des tests d’acceptation avant le développement, avec la contribution des parties prenantes ;
- **Développement piloté par le comportement** (_Behavior-Driven Development_, **BDD**) : l’équipe décrit le comportement attendu dans un langage partagé et compréhensible par les personnes techniques et non techniques.

Ces approches favorisent la clarification des attentes et des retours rapides. Elles ne remplacent pas tous les autres tests : il faut choisir les activités de test selon le contexte et les risques.

## 7. Décaler les tests vers la gauche (Shift-left Testing)

Le **décalage des tests vers la gauche** (_shift-left testing_) consiste à commencer certaines activités de test plus tôt dans le cycle de développement, plutôt que d’attendre la fin.

Cela peut inclure :

- relire les exigences dès leur rédaction ;
- examiner les conceptions et les maquettes ;
- préparer les tests avant que la fonction soit terminée ;
- automatiser des vérifications qui donnent un retour rapide ;
- collaborer tôt entre testeurs, développeurs et personnes métier.

Le but est de détecter et clarifier les problèmes plus tôt. Le décalage vers la gauche ne signifie pas qu’on peut supprimer les tests tardifs ou les tests du produit complet.

## 8. Tests et DevOps (Testing with DevOps)

**DevOps** est un mot-valise formé à partir de _Development_ (développement) et _Operations_ (exploitation). Cette approche rapproche les équipes de développement et d’exploitation afin de livrer et d’exploiter le logiciel plus efficacement.

Dans un contexte DevOps, les tests sont souvent intégrés à des processus automatisés de construction et de livraison. Cela permet d’obtenir rapidement des retours sur les changements.

L’automatisation est utile, mais elle ne suffit pas à elle seule : l’équipe doit aussi choisir les bons tests, analyser les résultats et tenir compte des risques.

## 9. Tests de maintenance (Maintenance Testing)

Les **tests de maintenance** (_maintenance testing_) sont effectués lorsqu’un logiciel déjà livré est modifié ou lorsque son environnement change.

Ils peuvent être déclenchés par :

- une correction de défaut ;
- une nouvelle fonctionnalité ou une amélioration ;
- une migration vers un nouvel environnement ou une nouvelle plateforme ;
- le retrait d’une fonctionnalité ;
- un changement de configuration ou d’infrastructure.

Après une modification, les tests doivent vérifier le comportement concerné et évaluer le risque de régression dans les parties qui n’étaient pas censées changer.

**Exemple :** après une mise à jour de la bibliothèque de paiement, l’équipe vérifie le paiement, mais aussi les parcours voisins susceptibles d’être affectés.

## 10. Mise en pratique (Practical Exercise)

Une équipe développe une boutique en ligne par versions. La version actuelle permet de consulter le panier. La prochaine version ajoute le paiement.

Pour préparer les tests, je peux me demander :

- Quels composants doivent être vérifiés séparément ?
- Quelles interactions entre le panier et le service de paiement faut-il tester ?
- Quel parcours complet vérifier au niveau système ?
- Quels critères permettront aux parties prenantes d’accepter la fonctionnalité ?
- Quels tests fonctionnels et non fonctionnels sont pertinents ?
- Quels tests existants faut-il rejouer pour détecter une régression ?
- Quelles exigences ou maquettes peut-on relire avant la fin du développement ?

Cet exercice montre qu’un même changement peut nécessiter plusieurs niveaux et types de test, ainsi que des activités avant et après le développement.

## 11. À retenir (Key Takeaways)

- Les tests s’intègrent au cycle de développement et ne commencent pas uniquement lorsque le code est terminé.
- Le modèle de cycle de vie influence le moment et l’organisation des activités de test.
- Les niveaux de test décrivent un périmètre et un objectif ; les types de test décrivent ce qui est vérifié.
- Les approches « test en premier » et le décalage vers la gauche favorisent les retours précoces.
- Les tests de maintenance sont déclenchés par des changements du logiciel ou de son environnement.
- L’automatisation soutient les tests, mais ne remplace ni l’analyse ni le jugement de l’équipe.

## 12. Pour vérifier ma compréhension (Knowledge Check)

1. Pourquoi est-il utile de tester des exigences avant que le code soit terminé ?
2. Quelle différence fais-tu entre un niveau de test et un type de test ?
3. Dans quel niveau testerais-tu l’interaction entre le panier et le service de paiement ?
4. « Vérifier le temps de réponse d’une application » correspond-il à un niveau ou à un type de test ?
5. Donne deux exemples de changements pouvant déclencher des tests de maintenance.
6. Le « décalage vers la gauche » signifie-t-il qu’on ne teste plus le logiciel complet à la fin ?

<details>
<summary>Correction proposée (Suggested Answers)</summary>

1. Pour détecter plus tôt les ambiguïtés ou les erreurs et obtenir des retours avant que le développement ne rende les changements plus coûteux.
2. Le niveau décrit le périmètre et l’objectif du test ; le type décrit le comportement ou la caractéristique vérifiée.
3. Au niveau d’intégration.
4. C’est un type de test non fonctionnel, généralement réalisé au niveau système, selon le périmètre choisi.
5. Une correction de défaut, une nouvelle fonctionnalité, une migration de plateforme ou le retrait d’une fonction.
6. Non. On commence certaines activités plus tôt, mais les tests tardifs et les tests du système complet restent nécessaires lorsqu’ils sont pertinents.

</details>

## Références et ressources (References and Resources)

- [ISTQB — Certified Tester Foundation Level (CTFL) v4.0](https://istqb.org/certifications/certified-tester-foundation-level) : syllabus officiel et examens blancs.
- [Manifeste Agile](https://agilemanifesto.org/iso/fr/manifesto.html) : valeurs et principes qui ont influencé les approches agiles.
- [Glossaire ISTQB](https://glossary.istqb.org/) : définitions des termes liés aux niveaux, types et cycles de vie de test.
- [CFTL — Comité Français des Tests Logiciels](https://cftl.fr/) : ressources et informations sur les tests logiciels en français.
- [GitHub Docs — Intégration continue avec GitHub Actions](https://docs.github.com/en/actions/automating-builds-and-tests/about-continuous-integration) : exemple de pipeline qui construit le projet et exécute les tests à chaque changement.

_Cette fiche est une synthèse personnelle destinée à l’apprentissage. En cas de différence de formulation, se référer au syllabus ISTQB officiel et aux supports de formation._
