# Gestion des activités de test (Managing the Test Activities)

## Objectifs d’apprentissage (Learning Objectives)

À la fin de cette fiche, je dois pouvoir :

- expliquer les objectifs et le contenu d’un plan de test ;
- prioriser les tests selon les risques ;
- distinguer le suivi, le contrôle et l’achèvement des tests ;
- expliquer l’intérêt de la gestion de configuration et de la gestion des défauts ;
- reconnaître les informations utiles pour communiquer l’avancement et les résultats.

## 1. Planification des tests (Test Planning)

La **planification des tests** (_test planning_) consiste à définir les objectifs, l’approche, les ressources et les activités nécessaires pour tester un produit dans un contexte donné. Le plan peut être un document formel ou un ensemble d’informations maintenues dans les outils et pratiques de l’équipe.

Un plan de test peut notamment préciser :

- le périmètre des tests et leurs objectifs ;
- les éléments à tester et ceux qui sont hors périmètre ;
- l’approche de test, les niveaux et les types de test retenus ;
- les critères d’entrée et de sortie ;
- les responsabilités et les compétences nécessaires ;
- les ressources, l’environnement et les données de test ;
- le calendrier, les dépendances et les contraintes ;
- les risques liés au produit et au projet, ainsi que les réponses prévues ;
- la manière de suivre l’avancement et de communiquer les résultats.

La planification est évolutive : les estimations et les décisions peuvent être ajustées lorsque l’équipe apprend davantage sur le produit, les risques ou les contraintes.

### Critères d’entrée et de sortie (Entry and Exit Criteria)

Les **critères d’entrée** (_entry criteria_) définissent les conditions à réunir pour commencer une activité de test de manière efficace. Par exemple, l’environnement nécessaire est disponible et la version à tester est identifiée.

Les **critères de sortie** (_exit criteria_) définissent les conditions à satisfaire pour considérer une activité de test comme terminée. Ils peuvent porter sur la couverture attendue, les tests exécutés, les défauts restants ou le niveau de risque accepté.

Les critères de sortie ne signifient pas nécessairement que tous les défauts sont corrigés. Une décision de fin peut tenir compte des défauts connus, de leur sévérité, des risques résiduels et des contraintes de livraison.

### Estimation et approche de test (Estimation and Test Approach)

L’**estimation des tests** (_test estimation_) prévoit les efforts, les coûts et la durée nécessaires. Elle s’appuie sur les informations disponibles, telles que la taille et la complexité du périmètre, les risques, les compétences, les données et les environnements requis, ainsi que les résultats des travaux précédents.

Une estimation est une prévision, pas une garantie. Elle peut être révisée lorsque le périmètre ou les hypothèses changent.

L’**approche de test** (_test approach_) décrit comment les objectifs seront atteints. Elle peut préciser les techniques, les niveaux, les types de test, le degré d’automatisation et la manière d’adapter les activités au contexte.

## 2. Gestion des risques (Risk Management)

Un **risque** (_risk_) est un événement ou une situation incertaine qui pourrait avoir un effet négatif. En test, on distingue souvent :

- le **risque produit** (_product risk_), lié à un défaut possible du produit et à ses conséquences ;
- le **risque projet** (_project risk_), lié à la capacité de réaliser le travail, par exemple un retard, un manque de ressources ou un environnement indisponible.

### Analyse du risque produit (Product Risk Analysis)

L’analyse du risque produit aide à décider **quoi tester en priorité**, avec quelle profondeur et quels moyens. L’équipe identifie les risques, estime leur probabilité et leur impact, puis leur attribue une priorité.

La priorité d’un risque produit est souvent déterminée à partir de :

- la **probabilité** qu’un défaut existe ou se manifeste ;
- l’**impact** si le défaut affecte les utilisateurs, l’entreprise, la conformité ou la sécurité.

Une zone à risque élevé justifie généralement des tests plus précoces, plus approfondis ou plus fréquents. Cette priorisation ne signifie pas que les zones à faible risque ne seront jamais testées : elle aide à répartir les ressources disponibles.

**Exemple :** dans une boutique en ligne, un défaut du calcul du paiement peut entraîner des pertes financières et avoir une probabilité importante après une modification récente. Ce risque mérite une priorité élevée par rapport à un défaut mineur dans un texte secondaire.

### Contrôle des risques (Risk Control)

Le contrôle des risques consiste à choisir et à mettre en œuvre des actions pour réduire les risques. Les actions peuvent inclure :

- des tests visant à prévenir ou détecter les défauts ;
- des revues des exigences ou de la conception ;
- une surveillance renforcée des zones à risque ;
- des mesures de réduction d’impact, comme une livraison progressive ou un plan de retour arrière.

La priorité peut évoluer quand de nouvelles informations apparaissent ou qu’un changement modifie la probabilité ou l’impact d’un risque.

## 3. Suivi, contrôle et achèvement des tests (Test Monitoring, Control and Completion)

Ces activités permettent de comparer l’avancement réel aux objectifs prévus et d’agir lorsque la situation change.

### Suivi des tests (Test Monitoring)

Le **suivi des tests** (_test monitoring_) consiste à recueillir et analyser des informations sur l’avancement et la qualité. Des indicateurs possibles incluent :

- le nombre de tests prévus, exécutés, réussis, échoués ou bloqués ;
- la couverture des exigences ou des risques ;
- le nombre de défauts ouverts, corrigés ou réouverts ;
- les efforts et le calendrier consommés par rapport aux prévisions.

Un indicateur doit être interprété avec son contexte. Par exemple, un grand nombre de tests réussis ne démontre pas à lui seul que les risques importants sont couverts.

### Contrôle des tests (Test Control)

Le **contrôle des tests** (_test control_) utilise les informations du suivi pour prendre des décisions et ajuster les activités. L’équipe peut modifier les priorités, réallouer des ressources, ajouter des tests, revoir le calendrier ou communiquer un risque de livraison.

Le contrôle ne consiste donc pas seulement à mesurer : il transforme les constats en actions.

### Achèvement des tests (Test Completion)

L’**achèvement des tests** (_test completion_) regroupe les activités réalisées à la fin d’une phase, d’un niveau ou d’un projet de test. Il peut comprendre :

- vérifier les résultats par rapport aux critères de sortie ;
- résumer les tests exécutés, la couverture et les défauts connus ;
- consigner les risques résiduels et les écarts au plan ;
- archiver les éléments utiles, comme les cas de test, les données et les rapports ;
- transmettre les informations pertinentes aux personnes qui maintiendront le produit ;
- noter les enseignements à réutiliser dans les activités futures.

Une activité de test peut être achevée même si certains défauts restent ouverts, à condition que leur état et les risques associés soient communiqués et qu’une décision appropriée soit prise.

## 4. Gestion de configuration (Configuration Management)

La **gestion de configuration** (_configuration management_) identifie et contrôle les versions des éléments qui composent le produit et son environnement. Elle aide à savoir précisément ce qui a été testé et à reproduire les résultats.

Les éléments concernés peuvent inclure :

- le code et les composants logiciels ;
- les exigences et les autres documents de référence ;
- les cas de test et les données de test ;
- les configurations et les environnements ;
- les versions des outils ou des dépendances lorsqu’elles influencent les résultats.

Un résultat de test devrait pouvoir être associé à une version précise du produit, à un environnement et aux données utilisées. Sans cette traçabilité, il peut être difficile de reproduire une défaillance ou de déterminer si une correction a été testée.

## 5. Gestion des défauts (Defect Management)

Un **rapport de défaut** (_defect report_) communique un problème observé ou suspecté de façon à permettre son analyse et son suivi. Il doit être compréhensible, factuel et suffisamment détaillé pour aider à reproduire le problème.

Un rapport comprend souvent :

- un identifiant et un titre descriptif ;
- le contexte et la version testée ;
- les étapes pour reproduire le problème ;
- le résultat attendu et le résultat observé ;
- les données et l’environnement utilisés ;
- des éléments de preuve, lorsque c’est utile ;
- une évaluation de la sévérité et de la priorité, selon le processus de l’équipe ;
- l’état du défaut et les personnes ou équipes concernées.

La **sévérité** (_severity_) décrit l’impact du défaut sur le produit ou ses utilisateurs. La **priorité** (_priority_) indique l’urgence ou l’ordre dans lequel l’équipe devrait traiter le défaut. Ces notions sont liées, mais elles ne sont pas synonymes : un défaut très visible peut être prioritaire sans avoir un impact fonctionnel majeur, tandis qu’un défaut grave dans un parcours rare peut demander une analyse de risque.

Le cycle de vie d’un défaut varie selon les équipes, mais peut inclure les états suivants : signalé, analysé, accepté, assigné, corrigé, retesté, fermé ou rouvert. Une équipe peut aussi rejeter un rapport s’il ne décrit pas un défaut reproductible ou s’il correspond au comportement attendu ; la décision doit alors être expliquée.

Après une correction, le **retest** vérifie que le défaut concerné est corrigé. Des tests de régression examinent ensuite les zones susceptibles d’avoir été affectées par le changement.

### Outils professionnels de gestion des tests (Professional Test Management Tools)

Dans les équipes professionnelles, les tests peuvent être organisés dans un outil de gestion dédié ou dans la plateforme de développement déjà utilisée par l’équipe. Ces outils peuvent centraliser les plans, les suites et les cas de test, les exécutions, les résultats, les défauts associés et les rapports. Ils soutiennent le processus ; ils ne définissent pas à eux seuls une bonne stratégie de test.

Exemples de solutions utilisées en contexte d’équipe :

- **Azure Test Plans** : intégré à Azure DevOps ; permet de structurer les plans, suites et cas de test, d’exécuter des tests manuels ou exploratoires, et de relier exigences, résultats et défauts.
- **Zephyr** : solution de gestion des tests intégrée à Jira ; organise les cas, cycles d’exécution et plans, avec suivi de progression et traçabilité.
- **TestRail** : gestionnaire de tests spécialisé ; centralise cas, plans, exécutions et résultats, et peut être relié à des outils de suivi comme Jira ou Azure DevOps.

Le choix dépend notamment de l’écosystème déjà en place, du niveau de traçabilité recherché, des besoins de reporting, du mode d’hébergement, du budget et des exigences de sécurité. Ces produits ont des offres et conditions qui peuvent évoluer ; il faut vérifier les fonctionnalités, tarifs et contraintes actuels auprès de leurs éditeurs.

## 6. Mise en pratique (Practical Exercise)

Une équipe prépare la livraison d’une nouvelle version de sa boutique en ligne. Le paiement par carte et le calcul des montants ont été modifiés. Un défaut d’affichage a aussi été signalé sur une page secondaire. L’environnement de test a été indisponible une journée, et plusieurs tests de paiement échouent encore à la veille de la livraison. La version candidate et les données utilisées doivent être communiquées à une autre équipe pour la maintenance.

Pour organiser les activités :

- identifie un risque produit élevé et un risque projet ;
- propose des critères d’entrée et de sortie adaptés aux tests de paiement ;
- indique quels tests devraient être priorisés et justifie ce choix ;
- propose des informations à suivre et une action de contrôle en réponse aux échecs ;
- décris les éléments à archiver ou transmettre à la fin des tests ;
- rédige les principales informations à inclure dans un rapport de défaut de paiement ;
- distingue le retest de la correction des tests de régression à effectuer.

## 7. À retenir (Key Takeaways)

- La planification définit les objectifs, le périmètre, l’approche, les ressources, le calendrier et les critères de test.
- Les risques produit orientent la priorité et la profondeur des tests ; les risques projet menacent la réalisation des activités.
- Le suivi recueille les informations, le contrôle entraîne des décisions et des ajustements, et l’achèvement consigne les résultats et les éléments à transmettre.
- La gestion de configuration permet d’identifier exactement les versions et environnements testés.
- Un rapport de défaut doit être clair, reproductible et contextualisé ; sévérité et priorité décrivent deux aspects différents.
- Le retest vérifie la correction d’un défaut, tandis que la régression recherche les effets indésirables des changements.

## 8. Pour vérifier ma compréhension (Knowledge Check)

1. À quoi servent les critères d’entrée et de sortie ?
2. Quelle est la différence entre risque produit et risque projet ?
3. Comment l’analyse des risques peut-elle influencer la priorité des tests ?
4. Quelle différence fais-tu entre suivi et contrôle des tests ?
5. Pourquoi associer un résultat de test à une version et à un environnement précis ?
6. Quelle différence y a-t-il entre sévérité et priorité d’un défaut ?
7. Après une correction, que vérifie le retest et que cherchent les tests de régression ?
8. Peut-on achever les tests avec des défauts encore ouverts ? Quelles précautions prendre ?

<details>
<summary>Correction proposée (Suggested Answers)</summary>

1. Les critères d’entrée déterminent si les conditions permettent de commencer une activité ; les critères de sortie définissent les conditions pour la considérer terminée.
2. Le risque produit concerne les conséquences possibles de défauts dans le produit ; le risque projet concerne les événements pouvant compromettre la réalisation du travail.
3. Les zones à forte probabilité et à fort impact reçoivent généralement des tests plus prioritaires ou plus approfondis.
4. Le suivi recueille et analyse l’avancement ; le contrôle utilise ces informations pour décider d’actions et ajuster le travail.
5. Pour savoir précisément ce qui a été testé, reproduire les résultats et déterminer si une correction s’applique à la version concernée.
6. La sévérité décrit l’impact du défaut ; la priorité décrit l’urgence de son traitement.
7. Le retest vérifie que le défaut signalé est corrigé ; les tests de régression vérifient que les changements n’ont pas créé de problèmes ailleurs.
8. Oui, selon les critères et la décision de l’équipe. Les défauts ouverts, leur impact, les risques résiduels et leur acceptation doivent être documentés et communiqués.

</details>

## Références et ressources (References and Resources)

- [ISTQB — Syllabus CTFL v4.0.1](https://istqb.org/?sdm_process_download=1&download_id=3345) : chapitre 5, « Managing the Test Activities », sur la planification, les risques, le suivi et le contrôle, l’achèvement, la configuration et les défauts.
- [Glossaire ISTQB](https://glossary.istqb.org/) : définitions des termes de gestion des tests, des risques, de la configuration et des défauts.
- [Microsoft Learn — Présentation d’Azure Test Plans](https://learn.microsoft.com/en-us/azure/devops/test/overview?view=azure-devops) : plans, suites, cas, exécutions manuelles et exploratoires, résultats et traçabilité.
- [SmartBear — Présentation des plans de test Zephyr](https://support.smartbear.com/zephyr/docs/en/test-plans/test-plans--overview-.html) : organisation des cycles, suivi de l’avancement, métriques et couverture.
- [TestRail — Gestion des tests](https://www.testrail.com/test-management/) : exemple de gestionnaire spécialisé pour planifier, assigner et suivre les cas, exécutions et résultats.
- [GitHub Docs — Démarrage avec GitHub Issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart) : exemple de suivi d’un défaut avec titre, étapes de reproduction, résultats attendus et observés, étiquettes et affectation. Un outil de tickets ne remplace pas toujours un gestionnaire de cas et de campagnes de test.

_Cette fiche est une synthèse personnelle destinée à l’apprentissage. En cas de différence de formulation, se référer au syllabus ISTQB officiel et aux supports de formation._
