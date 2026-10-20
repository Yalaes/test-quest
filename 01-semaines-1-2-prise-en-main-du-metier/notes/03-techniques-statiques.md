# Techniques statiques (Static Testing)

## Objectifs d’apprentissage (Learning Objectives)

À la fin de cette fiche, je dois pouvoir :

- expliquer ce que sont les tests statiques et les distinguer des tests dynamiques ;
- citer les avantages et les limites des techniques statiques ;
- décrire les principales étapes, les rôles et les types de revue ;
- expliquer le rôle des outils d’analyse statique.

## 1. Qu’est-ce que le test statique ? (What Is Static Testing?)

Le **test statique** (_static testing_) consiste à évaluer un produit logiciel ou un autre élément de travail **sans exécuter le logiciel**. Il peut être réalisé par des personnes, au moyen de revues, ou avec des outils d’analyse statique.

Les éléments examinés peuvent notamment être :

- des exigences, des récits utilisateurs ou des critères d’acceptation ;
- des modèles, des conceptions ou des maquettes ;
- du code source ;
- des plans, des cas de test ou des scripts de test ;
- de la documentation utilisateur ou technique.

Une revue peut repérer, par exemple, une exigence ambiguë. Un outil d’analyse statique peut signaler une variable inutilisée dans le code. Dans les deux cas, le logiciel n’a pas besoin d’être lancé.

### Test statique et test dynamique (Static and Dynamic Testing)

Le **test dynamique** (_dynamic testing_) nécessite l’exécution du logiciel. Il permet d’observer son comportement et de constater des défaillances dans les conditions du test.

| Test statique                                                               | Test dynamique                                                      |
| --------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| N’exécute pas le logiciel.                                                  | Exécute le logiciel.                                                |
| Évalue directement un élément de travail, comme une exigence ou du code.    | Évalue le comportement du logiciel en exécution.                    |
| Peut révéler des omissions, des ambiguïtés ou des défauts dans un livrable. | Peut révéler des défaillances qui apparaissent pendant l’exécution. |

Les deux approches sont complémentaires : une revue d’exigences ne prouve pas que le logiciel se comporte correctement à l’exécution, et un test dynamique ne repère pas nécessairement toutes les ambiguïtés des exigences.

## 2. Avantages des tests statiques (Benefits of Static Testing)

Les techniques statiques peuvent :

- détecter des défauts tôt, avant que le code ou les tests dépendants soient terminés ;
- éviter la propagation d’un défaut vers les étapes suivantes ;
- repérer des problèmes difficiles à trouver par l’exécution seule, comme une exigence manquante ou une documentation contradictoire ;
- améliorer la compréhension partagée des exigences et de la conception ;
- réduire les coûts de correction lorsque les problèmes sont traités tôt ;
- fournir des retours rapides et contribuer à améliorer la qualité des livrables.

La revue peut aussi transmettre des connaissances entre les personnes qui y participent et mettre en évidence les risques ou les désaccords tôt dans le projet.

### Limites et points de vigilance (Limitations and Considerations)

- Une revue dépend de la disponibilité et de l’expertise des participants.
- Un outil peut produire des alertes qui ne correspondent pas à un défaut réel ; les résultats doivent être analysés.
- Le test statique ne montre pas le comportement réel du logiciel pendant son exécution.
- Les tests statiques ne remplacent donc pas les tests dynamiques : le choix dépend du livrable, des risques et des objectifs.

## 3. Les revues (Reviews)

Une **revue** (_review_) est un examen d’un élément de travail par une ou plusieurs personnes afin de repérer des problèmes, d’améliorer sa qualité ou de prendre une décision. Les revues peuvent être plus ou moins formelles selon leur objectif, leur contexte et le processus suivi.

Une revue n’a pas toujours pour seul objectif de trouver des défauts. Elle peut aussi faciliter les échanges, vérifier la conformité à des critères ou permettre aux participants d’acquérir une compréhension commune.

### Facteurs de réussite d’une revue (Review Success Factors)

Une revue a davantage de chances d’être utile lorsque :

- son objectif et son périmètre sont clairs ;
- les participants disposent du temps et des compétences adaptés ;
- les éléments examinés sont suffisamment petits et compréhensibles ;
- les critères de revue sont définis, lorsque c’est pertinent ;
- les participants se préparent et se concentrent sur le produit, pas sur la personne qui l’a créé ;
- les défauts et les questions sont consignés de manière compréhensible ;
- les résultats et les actions à suivre sont communiqués.

Une revue ne doit pas devenir une recherche de fautes personnelles. Son but est d’améliorer le livrable et de soutenir la collaboration.

### Processus de revue (Review Process)

Le degré de formalité varie, mais une revue structurée comprend souvent les activités suivantes :

1. **Planification** : préciser l’objectif, le périmètre, les participants, les critères et le temps prévu.
2. **Démarrage de la revue** : partager l’élément de travail, le contexte, les consignes et les critères.
3. **Revue individuelle** : chaque participant examine l’élément et relève les anomalies ou les questions.
4. **Communication et analyse** : les points relevés sont clarifiés et analysés ; une réunion peut être organisée si nécessaire.
5. **Correction et compte rendu** : les défauts acceptés sont traités, puis le résultat et les éventuelles actions de suivi sont consignés.

La revue individuelle est importante : la réunion ne devrait pas être la première occasion de découvrir le contenu.

### Rôles dans une revue (Review Roles)

Selon le type de revue, une personne peut tenir plusieurs rôles :

- **Auteur** (_author_) : crée ou maintient l’élément de travail examiné et apporte les clarifications nécessaires.
- **Responsable de revue** (_review leader_) : assume la responsabilité globale de la revue et de son déroulement.
- **Facilitateur** (_facilitator_) : aide le groupe à avancer efficacement et à respecter les règles de discussion.
- **Réviseur** (_reviewer_) : examine le livrable et signale les anomalies ou les questions liées à son expertise.
- **Scribe** (_scribe_) : consigne les points relevés, les décisions et les actions à suivre.

Dans une revue peu formelle, certains rôles peuvent être combinés ou ne pas être attribués explicitement.

### Types de revue (Review Types)

Les types de revue se distinguent par leur niveau de formalité, leur objectif et la manière dont les participants travaillent.

| Type                                     | Caractéristiques principales                                                                                                                                                              |
| ---------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Revue informelle** (_informal review_) | Pas de processus formel défini. Elle peut prendre la forme d’une relecture par un collègue ou d’une discussion rapide.                                                                    |
| **Walkthrough** (_walkthrough_)          | L’auteur guide les participants à travers le livrable. Le groupe pose des questions et peut relever des problèmes ; cette revue favorise aussi le partage de connaissances.               |
| **Revue technique** (_technical review_) | Des personnes qualifiées examinent le livrable et prennent des décisions ou formulent des recommandations techniques selon des critères convenus. Un facilitateur est généralement utile. |
| **Inspection** (_inspection_)            | Revue formelle et structurée, avec des rôles et des règles définis, une préparation individuelle et la consignation des anomalies. Elle vise notamment à détecter les défauts.            |

Ces appellations peuvent varier selon les organisations. L’important est de comprendre le degré de structure et l’objectif de la revue choisie.

## 4. Analyse statique (Static Analysis)

L’**analyse statique** (_static analysis_) utilise généralement un outil pour examiner un élément de travail sans exécuter le logiciel. Elle est souvent appliquée au code source, mais peut aussi s’appliquer à d’autres artefacts selon les outils.

Un outil peut notamment signaler :

- des violations de règles de codage ou de conventions ;
- du code inaccessible ou des variables inutilisées ;
- des constructions potentiellement risquées ou des défauts de programmation ;
- certains problèmes de sécurité ou de maintenabilité.

Les résultats sont des **alertes à analyser**, pas nécessairement des défauts confirmés. Une personne doit décider si l’alerte est pertinente, si le code doit être corrigé ou si la règle doit être ajustée.

L’analyse statique peut être intégrée à l’environnement de développement ou à un processus automatisé de construction. Des retours fréquents permettent de traiter les problèmes près du moment où ils sont introduits.

### Revue ou analyse statique ? (Review or Static Analysis?)

- Une **revue** s’appuie sur l’examen humain et le dialogue entre les participants.
- Une **analyse statique** est généralement effectuée par un outil selon des règles configurées.
- Les deux peuvent examiner le même élément et se compléter : l’outil détecte certains motifs, tandis que les personnes évaluent le sens, le contexte et les besoins métier.

## 5. Mise en pratique (Practical Exercise)

Une équipe prépare une nouvelle fonction de remboursement. Avant le développement, elle examine une exigence qui indique : « Le remboursement est traité rapidement. » Après le développement, un outil signale qu’une branche du code ne peut jamais être atteinte.

Pour analyser ces situations :

- La relecture de l’exigence est-elle statique ou dynamique ? Pourquoi ?
- Quel problème peut-on relever dans l’expression « rapidement » ?
- Le signalement de l’outil confirme-t-il automatiquement un défaut ?
- Quels tests dynamiques restent nécessaires après ces activités ?

## 6. À retenir (Key Takeaways)

- Le test statique examine un livrable sans exécuter le logiciel ; le test dynamique nécessite son exécution.
- Les revues reposent principalement sur l’examen humain ; l’analyse statique est généralement outillée.
- Les tests statiques peuvent repérer tôt des défauts et des problèmes qui ne sont pas facilement observables à l’exécution.
- Une revue utile a un objectif clair, des participants adaptés et des résultats suivis.
- Les alertes d’analyse statique doivent être interprétées ; elles ne prouvent pas toutes l’existence d’un défaut.
- Les techniques statiques et dynamiques sont complémentaires.

## 7. Pour vérifier ma compréhension (Knowledge Check)

1. Quelle est la différence essentielle entre test statique et test dynamique ?
2. Donne deux exemples d’éléments de travail pouvant faire l’objet d’une revue.
3. Une exigence ambiguë peut-elle être repérée par un test dynamique ? Quelle technique est particulièrement adaptée ?
4. Quelle différence fais-tu entre une revue et une analyse statique ?
5. Une alerte générée par un outil d’analyse statique est-elle toujours un défaut confirmé ?
6. Quel type de revue est généralement le plus formel et structuré ?
7. Les tests statiques rendent-ils inutiles les tests dynamiques ?

<details>
<summary>Correction proposée (Suggested Answers)</summary>

1. Le test statique n’exécute pas le logiciel ; le test dynamique l’exécute pour observer son comportement.
2. Par exemple : exigences, conception, code source, cas de test ou documentation.
3. Une revue statique de l’exigence est particulièrement adaptée. Un test dynamique peut révéler des conséquences d’une ambiguïté, mais il ne remplace pas l’examen du texte de l’exigence.
4. Une revue s’appuie principalement sur des personnes qui examinent un livrable ; l’analyse statique est généralement effectuée par un outil sans exécuter le logiciel.
5. Non. Il faut analyser l’alerte dans son contexte ; elle peut être non pertinente ou ne pas correspondre à un défaut réel.
6. L’inspection.
7. Non. Les approches sont complémentaires et permettent de détecter des problèmes différents.

</details>

## Références et ressources (References and Resources)

- [ISTQB — Syllabus CTFL v4.0.1](https://istqb.org/?sdm_process_download=1&download_id=3345) : chapitre 3, « Static Testing », notamment les bases des tests statiques et le processus de revue.
- [Glossaire ISTQB](https://glossary.istqb.org/) : vérifier les définitions de « static testing », « static analysis », « review » et des différents types de revue abordés dans cette fiche.
- [ESLint — À propos](https://eslint.org/docs/latest/about/) : exemple de linter et d’analyse statique pour JavaScript, qui repère certains motifs problématiques sans exécuter le code.

_Cette fiche est une synthèse personnelle destinée à l’apprentissage. En cas de différence de formulation, se référer au syllabus ISTQB officiel et aux supports de formation._
