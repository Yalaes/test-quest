# Agile — User stories, rétrospectives et planification

## Objectifs

- contribuer à la création collaborative d’une user story ;
- comprendre le rôle des critères d’acceptation ;
- expliquer le but d’une rétrospective ;
- distinguer planification de release et planification d’itération.

## 1. User stories

Une **user story** est une courte description d’un besoin du point de vue de la personne qui en bénéficiera. Un format courant est :

> En tant que **[type d’utilisateur]**, je veux **[capacité]**, afin de **[bénéfice]**.

La story sert de support à la conversation et ne remplace pas les échanges nécessaires pour comprendre le besoin.

### Critères d’acceptation

Les **critères d’acceptation** décrivent les conditions observables qui permettront de vérifier si le besoin est satisfait. Ils doivent être compris par l’équipe et les parties prenantes.

Un exemple peut utiliser le format **Étant donné / Quand / Alors** :

- **Étant donné** un contexte ;
- **Quand** une action se produit ;
- **Alors** un résultat observable est attendu.

### Collaboration

La création collaborative d’une story peut inclure la personne responsable du produit, les utilisateurs ou leurs représentants, les développeurs et les testeurs. La discussion permet de clarifier les cas habituels, les exceptions, les dépendances et les risques.

## 2. Rétrospectives

Une **rétrospective** est un événement d’équipe consacré à l’inspection de la manière de travailler et à l’identification d’améliorations possibles.

Une rétrospective utile :

- porte sur une période ou une itération définie ;
- donne la parole aux membres de l’équipe ;
- traite les difficultés sans chercher des coupables ;
- aboutit à une ou plusieurs actions concrètes ;
- vérifie lors d’une réunion ultérieure si les actions ont aidé.

Les rétrospectives visent l’amélioration du processus, pas l’évaluation individuelle des personnes.

## 3. Planification de release et d’itération

La **planification de release** organise les objectifs et les livraisons envisagées sur un horizon plus large. Elle tient compte de la valeur, des dépendances, des risques et des contraintes, et peut être révisée lorsque le contexte change.

La **planification d’itération** sélectionne les éléments de travail qu’une équipe prévoit de réaliser dans une itération, ainsi que son objectif. La capacité réelle, les dépendances et les critères d’acceptation influencent cette sélection.

La planification n’est pas une garantie que tout sera livré à date fixe : les prévisions doivent être réévaluées à partir de l’avancement et des retours.

## 4. Rôle des tests dans ces pratiques

- Les testeurs participent à la clarification des stories et à la conception des exemples.
- Les risques et besoins de test peuvent contribuer à l’estimation et à la sélection du travail.
- Les résultats des tests apportent des informations à l’équipe avant une décision de release.
- Les problèmes de qualité ou de collaboration peuvent devenir des sujets d’amélioration en rétrospective.

## À retenir

- Une story est un support à la conversation ; ses critères d’acceptation rendent le comportement attendu vérifiable.
- La rétrospective améliore la manière de travailler grâce à des actions suivies.
- Une release porte sur une livraison plus large ; une itération porte sur un objectif à court terme.
- Les tests contribuent à la planification, à l’évaluation des risques et aux retours de l’équipe.

## Révision

1. Pourquoi une user story ne suffit-elle pas toujours à décrire tous les cas à tester ?
2. Donne un exemple de critère d’acceptation observable.
3. Quelle différence fais-tu entre une planification de release et une planification d’itération ?
4. Comment vérifier qu’une rétrospective a produit une amélioration concrète ?

<details>
<summary>Correction proposée</summary>

1. Une user story est un rappel concis d’un besoin, pas une spécification exhaustive. Les règles, exceptions, données et résultats attendus doivent être clarifiés avec les parties prenantes et exprimés dans des critères d’acceptation ou des exemples.
2. Exemple : « Étant donné un panier contenant un produit disponible, quand le client confirme l’ajout, alors le produit apparaît dans le panier avec la quantité 1. » Le résultat est observable ; les règles précises dépendent du besoin du produit.
3. La planification de release porte sur des objectifs et livraisons à plus long terme ; la planification d’itération sélectionne le travail proche et l’objectif de l’itération, selon la capacité de l’équipe.
4. En définissant une action concrète, un responsable et une échéance, puis en vérifiant à l’itération suivante si l’action a été réalisée et si elle a amélioré la situation.

</details>

## Références et ressources

- [Le Guide Scrum — version française](https://scrumguides.org/docs/scrumguide/v2020/2020-Scrum-Guide-French.pdf) : objectifs et événements Scrum, dont la planification de sprint et la rétrospective.
- [Agile Alliance — User Stories](https://www.agilealliance.org/glossary/user-stories/) : définition, rôle de la conversation et pièges courants liés aux user stories.
