# Tests Agiles — Méthodes, techniques et outils

## Objectifs

- décrire les pratiques de test utiles dans une équipe Agile ;
- expliquer comment les tests s’intègrent aux itérations et à l’intégration continue ;
- sélectionner des techniques de test en fonction des risques et du besoin ;
- distinguer une pratique Agile d’un outil particulier.

## 1. Intégrer les tests au travail Agile

Les tests se déroulent tout au long du développement, plutôt qu’en une phase isolée à la fin. Les testeurs collaborent avec le reste de l’équipe pour comprendre le besoin, préparer les exemples, tester les incréments et communiquer les risques.

Quelques pratiques possibles :

- discuter des critères d’acceptation avant ou pendant le développement ;
- tester régulièrement les éléments terminés ;
- obtenir rapidement des retours sur les changements ;
- inclure les tests dans la définition de « terminé » de l’équipe ;
- conserver du temps pour les tests de régression, les défauts et l’exploration ;
- analyser les résultats et ajuster les priorités en fonction des risques.

## 2. Méthodes et techniques

Les techniques vues précédemment restent applicables en Agile : partitionnement en classes d’équivalence, valeurs limites, tables de décision, transitions d’état, revues, tests exploratoires et techniques basées sur les risques.

Les exemples d’acceptation peuvent aider l’équipe à partager une compréhension du comportement attendu. Les pratiques de développement piloté par les tests (TDD), de développement piloté par les tests d’acceptation (ATDD) et de développement piloté par le comportement (BDD) utilisent des tests ou exemples à différents niveaux et avec différentes collaborations ; elles ne sont pas synonymes.

À compléter selon le contenu du cours :

- méthode ou technique présentée ;
- moment où elle est utile ;
- participants concernés ;
- artefacts ou résultats produits ;
- risques et limites.

## 3. Intégration continue

L’**intégration continue** (_continuous integration_, **CI**) consiste à intégrer fréquemment les changements et à obtenir un retour régulier par des constructions et vérifications automatisées. Elle peut aider une équipe Agile à détecter des problèmes plus tôt.

Une CI ne rend pas automatiquement le produit correct : les vérifications doivent être adaptées, fiables et interprétées. Les tests manuels, l’exploration, les revues et les discussions sur le besoin restent importants.

Les outils spécifiques d’automatisation et la configuration des pipelines seront étudiés dans les modules concernés du programme.

## 4. Outils en contexte Agile

Un outil peut soutenir la collaboration ou rendre le travail visible, par exemple en organisant les stories, les critères, les défauts ou l’avancement. Le choix dépend du processus et de l’équipe ; l’outil ne rend pas une pratique Agile par lui-même.

À distinguer :

- une méthode ou une pratique décrit une façon de travailler ;
- une technique de test aide à concevoir les vérifications ;
- un outil fournit un support logiciel à certaines activités.

Les outils détaillés de gestion des tests sont présentés dans la note 06 de la partie « Fondamentaux des tests ». Les plateformes CI et les outils d’automatisation seront approfondis dans les semaines consacrées à DevOps et aux outils spécialisés.

## À retenir

- Agile intègre les tests aux activités régulières de l’équipe et encourage des retours fréquents.
- Les techniques de conception vues précédemment restent utiles ; elles sont choisies en fonction du contexte et des risques.
- TDD, ATDD et BDD ont des objectifs et des pratiques liés, mais ne sont pas interchangeables.
- La CI facilite des vérifications fréquentes sans garantir la qualité à elle seule.
- Un outil peut soutenir une pratique, mais ne la remplace pas.

## Révision

1. Pourquoi les tests doivent-ils être préparés avant la fin de l’itération ?
2. Donne un exemple de technique de test adaptée à une user story.
3. Quelle différence y a-t-il entre une technique de test, une pratique Agile et un outil ?
4. Quelles activités humaines restent utiles même si la CI exécute des vérifications automatiquement ?

<details>
<summary>Correction proposée</summary>

1. Tester pendant l’itération permet de détecter tôt une incompréhension ou un défaut, de fournir un retour à l’équipe et d’ajuster le travail avant qu’il ne soit trop tard pour agir.
2. Pour une règle de quantité minimale ou maximale dans une story, le partitionnement en classes d’équivalence et l’analyse des valeurs limites peuvent aider à sélectionner des exemples.
3. Une pratique Agile décrit une façon de collaborer ou d’organiser le travail ; une technique de test aide à concevoir des vérifications ; un outil est un logiciel qui soutient certaines activités.
4. La clarification des besoins, les revues, les tests exploratoires, l’analyse des résultats et des risques, ainsi que les décisions de priorité et de livraison restent des activités humaines importantes.

</details>

## Références et ressources

- [ISTQB — Syllabus CTFL v4.0.1](https://istqb.org/?sdm_process_download=1&download_id=3345) : chapitres sur le test dans le cycle de vie logiciel, les approches collaboratives et les outils de support.
- [Manifeste Agile — version française](https://agilemanifesto.org/iso/fr/manifesto.html) : valeurs qui orientent la collaboration et l’adaptation du travail.
- [Le Guide Scrum — version française](https://scrumguides.org/docs/scrumguide/v2020/2020-Scrum-Guide-French.pdf) : cadre Scrum et événements associés à l’inspection et à l’adaptation.
