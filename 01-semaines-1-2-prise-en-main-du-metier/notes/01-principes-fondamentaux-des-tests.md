# Principes fondamentaux des tests

## Objectifs d’apprentissage

À la fin de cette fiche, je dois pouvoir :

- expliquer ce que sont les tests logiciels et pourquoi ils sont nécessaires ;
- distinguer une erreur humaine, un défaut logiciel et une défaillance ;
- expliquer les sept principes fondamentaux des tests ;
- appliquer ces principes à un exemple concret.

## 1. Qu’est-ce que le test logiciel ?

Le test logiciel regroupe les activités qui permettent d’évaluer un logiciel et les éléments qui lui sont associés, afin d’en vérifier la qualité et de détecter des défauts.

Tester ne consiste pas seulement à exécuter un programme. Les activités de test peuvent aussi inclure :

- analyser les exigences et les autres documents ;
- concevoir des cas de test ;
- préparer les données et l’environnement de test ;
- exécuter les tests ;
- comparer les résultats obtenus aux résultats attendus ;
- analyser et communiquer les résultats.

Un test peut donc être réalisé **sans exécuter le logiciel** : par exemple, en relisant une exigence pour repérer une ambiguïté.

### Test et débogage : quelle différence ?

Le **test** cherche à révéler des défauts ou à évaluer la qualité du produit.

Le **débogage** consiste à rechercher la cause d’une défaillance, à localiser le défaut dans le code et à le corriger. Il est généralement effectué par les développeurs, même si les testeurs fournissent des informations utiles pour l’investigation.

**Exemple :** un test révèle qu’une commande est facturée deux fois. Le testeur décrit et signale la défaillance. Le développeur examine ensuite le code, trouve la cause et la corrige : c’est le débogage.

## 2. Pourquoi tester ?

Un défaut logiciel peut provoquer des conséquences très différentes : un désagrément mineur, une perte financière, une atteinte à la réputation ou, dans certains domaines, un risque pour la sécurité des personnes.

Les tests permettent notamment de :

- vérifier si le logiciel répond aux exigences ;
- évaluer s’il répond aux besoins des utilisateurs ;
- révéler des défauts avant la mise en production ;
- réduire les risques liés à la qualité ;
- fournir aux parties prenantes des informations utiles à la prise de décision ;
- renforcer la confiance dans le produit.

Tester réduit les risques, mais ne garantit pas qu’un logiciel soit exempt de défauts.

## 3. Erreur, défaut et défaillance

Ces termes décrivent des notions différentes :

- **Erreur** : action ou décision humaine incorrecte.
- **Défaut** : imperfection dans un produit ou un document, par exemple une erreur dans le code ou une exigence incorrecte.
- **Défaillance** : comportement incorrect observé lors de l’exécution du logiciel.

Une erreur humaine peut introduire un défaut. Si ce défaut est exécuté dans certaines conditions, il peut provoquer une défaillance.

**Exemple :**

1. Une personne interprète mal la règle de remise : c’est une **erreur**.
2. Le code applique une remise de 20 % au lieu de 10 % : c’est un **défaut**.
3. Le client voit un prix trop bas lors de sa commande : c’est une **défaillance**.

La relation n’est pas toujours aussi directe : un défaut peut ne jamais être exécuté, et une défaillance peut avoir plusieurs causes.

## 4. Les sept principes fondamentaux des tests

### 1. Les tests montrent la présence de défauts, pas leur absence

Un test réussi indique que le comportement vérifié a fonctionné dans les conditions testées. Il ne prouve pas que le logiciel ne contient aucun défaut.

**Exemple :** vérifier une connexion avec un mot de passe valide ne prouve pas que tous les cas de connexion fonctionnent correctement.

### 2. Les tests exhaustifs sont impossibles

Tester toutes les entrées, combinaisons, configurations et séquences d’utilisation demanderait généralement trop de temps et de ressources.

Il faut donc choisir les tests les plus utiles en fonction des risques, des exigences, des utilisateurs et du temps disponible.

**Exemple :** un champ acceptant des nombres peut avoir des possibilités presque infinies. On choisira plutôt des valeurs représentatives et des limites importantes.

### 3. Tester tôt permet d’économiser du temps et de l’argent

Un défaut détecté tôt est souvent moins coûteux à corriger qu’un défaut découvert après la livraison du logiciel. Les tests peuvent commencer dès les premières étapes, par exemple avec la revue des exigences.

**Exemple :** repérer une règle de calcul ambiguë lors d’une revue évite qu’elle soit interprétée différemment par les développeurs et recodée plus tard.

### 4. Les défauts ont tendance à se regrouper

Une partie limitée du logiciel contient souvent une grande proportion des défauts découverts. Ces zones peuvent être complexes, fréquemment modifiées ou difficiles à comprendre.

Les résultats des tests précédents peuvent aider à identifier les zones qui méritent davantage d’attention.

**Exemple :** si plusieurs défauts sont trouvés dans le calcul des paiements, cette fonctionnalité peut justifier des tests supplémentaires.

### 5. Les tests s’usent

Répéter toujours les mêmes tests finit par révéler moins de nouveaux défauts. Les tests existants restent utiles, notamment pour vérifier les régressions, mais il faut aussi les revoir et en concevoir de nouveaux.

**Exemple :** après plusieurs versions sans changement des tests de recherche, ajouter des cas portant sur les accents, les caractères spéciaux ou les résultats très nombreux peut améliorer la couverture.

### 6. Les tests dépendent du contexte

La manière de tester dépend du produit, de son usage, des risques, des contraintes et des personnes concernées.

**Exemple :** une application médicale, un jeu vidéo et un site de commerce n’ont pas les mêmes risques ni les mêmes priorités de test.

### 7. L’absence de défauts ne garantit pas que le produit soit utile

Un logiciel peut respecter ses spécifications tout en ne répondant pas au besoin réel des utilisateurs. Il faut donc vérifier à la fois la conformité aux exigences et l’adéquation aux besoins.

**Exemple :** une application peut calculer correctement les frais de livraison selon la spécification, mais rester inutilisable si les utilisateurs ne trouvent pas comment choisir leur adresse.

## 5. Mise en pratique

Une boutique en ligne propose un code promotionnel. Le code doit appliquer 10 % de réduction, une seule fois par commande.

Avant de tester, je peux me poser les questions suivantes :

- Que signifie « une seule fois par commande » : un seul code ou une seule réduction ?
- Que doit-il se passer si le code est expiré ou inconnu ?
- Le montant de la réduction est-il arrondi ? Si oui, comment ?
- Que se passe-t-il si le code est saisi plusieurs fois ?
- Quels cas présentent le plus de risques pour l’utilisateur ou l’entreprise ?

Cet exemple illustre plusieurs principes : les tests exhaustifs sont impossibles, les exigences doivent être comprises tôt, et la priorité des tests dépend des risques et du contexte.

## 6. À retenir

- Tester consiste à évaluer un produit et à chercher des informations sur sa qualité ; cela ne se limite pas à exécuter le logiciel.
- Les tests peuvent révéler des défauts, mais ne peuvent pas prouver leur absence.
- Une erreur humaine peut introduire un défaut, qui peut provoquer une défaillance.
- Les tests doivent être choisis selon les risques et le contexte.
- Un logiciel sans défaut connu n’est pas nécessairement utile aux utilisateurs.

## 7. Pour vérifier ma compréhension

1. Un test réussi prouve-t-il qu’il n’y a aucun défaut dans la fonctionnalité ?
2. Quelle est la différence entre un défaut et une défaillance ?
3. Pourquoi tester une exigence avant que le code soit écrit ?
4. Pourquoi faut-il faire évoluer les tests répétés d’une version à l’autre ?
5. Un logiciel conforme à ses exigences peut-il quand même décevoir ses utilisateurs ? Pourquoi ?

<details>
<summary>Correction proposée</summary>

1. Non. Il montre seulement que le comportement vérifié a réussi dans les conditions testées.
2. Le défaut est une imperfection dans le produit ; la défaillance est un comportement incorrect observé pendant l’exécution.
3. Pour repérer tôt les erreurs, ambiguïtés ou omissions, avant qu’elles ne coûtent davantage à corriger.
4. Parce que répéter uniquement les mêmes tests peut finir par révéler moins de nouveaux défauts. Il faut aussi adapter ou ajouter des tests.
5. Oui. Les exigences peuvent ne pas représenter correctement les besoins réels des utilisateurs.

</details>

## Références et ressources

- [ISTQB — Certified Tester Foundation Level (CTFL) v4.0](https://istqb.org/certifications/certified-tester-foundation-level) : syllabus officiel, structure du programme et exemples d’examens.
- [CFTL — Comprendre les tests](https://cftl.fr/tests-logiciels/comprendre-les-tests/) : ressources du Comité Français des Tests Logiciels, représentant de l’ISTQB en France.
- [Glossaire ISTQB](https://glossary.istqb.org/) : définitions normalisées du vocabulaire du test logiciel.

_Cette fiche est une synthèse personnelle destinée à l’apprentissage. En cas de différence de formulation, se référer au syllabus ISTQB officiel et aux supports de formation._
