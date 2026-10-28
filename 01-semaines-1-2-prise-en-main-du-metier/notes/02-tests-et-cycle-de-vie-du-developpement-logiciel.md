# Tester pendant le cycle de vie du développement logiciel (Testing Throughout the Software Development Life Cycle)

## Objectifs d’apprentissage (Learning Objectives)

À la fin de cette fiche, je dois pouvoir :

- expliquer pourquoi les tests doivent être adaptés au cycle de développement ;
- décrire comment les activités de test s’intègrent aux principaux modèles de cycle de vie ;
- distinguer les niveaux de test des types de test ;
- expliquer les approches « test en premier » et le principe du « décalage vers la gauche » ;
- reconnaître les principaux déclencheurs des tests de maintenance.

## 1. Le cycle de vie du développement logiciel (Software Development Life Cycle, SDLC)

## Les 7 phases du SDLC

## 1. Planning — Planification

Définir le problème, les objectifs, le budget, les risques et le périmètre.

## 2. Requirements Analysis — Analyse des besoins

Recueillir les exigences fonctionnelles et non fonctionnelles, les user stories et les critères d’acceptation.

## 3. Design — Conception

Définir l’architecture, la base de données, l’API, l’UX/UI et la sécurité.

## 4. Development — Développement

Écrire le code frontend et backend, intégrer les composants et versionner les changements.

## 5. Testing — Tests et assurance qualité

Vérifier les exigences, détecter les bugs, tester les intégrations et la sécurité.

## 6. Deployment — Déploiement

Livrer le logiciel dans l’environnement de production.

## 7. Maintenance — Maintenance et évolution

Surveiller le fonctionnement, corriger les bugs, mettre à jour et ajouter des fonctionnalités.

## SDLC --- Phase 1 : Planning (planification)

La phase de *Planning* consiste à déterminer ce que l'on veut
construire, pourquoi, pour qui, avec quels moyens et quelles
contraintes.

Prenons un exemple concret tout au long de l'explication : **une
application web de réservation de tables pour les restaurants**, simple
et abordable.

## 1. Définir le problème (*Define the problem*)

Il faut identifier la difficulté réelle que le logiciel doit résoudre.

Un problème n'est pas encore une solution technique.

**Exemple :**

-   Problème : les petits restaurants reçoivent leurs réservations par
    téléphone ou par messages, ce qui leur fait perdre du temps.
-   Conséquence : ils peuvent oublier des réservations, répondre
    tardivement ou avoir des doublons.
-   Besoin : disposer d'un moyen simple de centraliser les réservations.

Dire « je veux créer une application React » décrit une solution
technique, pas le problème à résoudre.

**Question à se poser :** quelle difficulté rencontrent les utilisateurs
aujourd'hui ?

## 2. Définir les objectifs (*Define the objectives*)

Un objectif décrit le résultat que le projet doit atteindre.

Il faut distinguer l'objectif du projet de la fonctionnalité qui
permettra de l'atteindre.

Exemple :

-   Objectif : réduire le temps consacré à la gestion des réservations.
-   Fonctionnalité : permettre aux clients de réserver une table en
    ligne.
-   Indicateur : mesurer le temps consacré à la gestion des réservations
    avant et après la mise en place du système.

Un bon objectif peut être mesurable. On utilise parfois la méthode SMART
: spécifique, mesurable, atteignable, pertinent et défini dans le temps.

Par exemple : « Réduire de 30 % le temps quotidien consacré à la gestion
des réservations après deux mois d'utilisation », si cet objectif est
réaliste et mesurable.

**Question à se poser :** comment saura-t-on que le projet a réussi ?

## 3. Identifier les utilisateurs (*Identify the users*)

Il faut savoir qui utilisera le logiciel et quels sont les besoins de
chaque catégorie d'utilisateurs.

On parle de *stakeholders* pour désigner les parties prenantes : toutes
les personnes ou organisations concernées par le projet, même si elles
n'utilisent pas directement l'application.

Dans notre exemple :

  -----------------------------------------------------------------------
  Acteur                              Besoin
  ----------------------------------- -----------------------------------
  Client                              Réserver une table facilement

  Restaurateur                        Consulter et gérer les réservations

  Administrateur                      Gérer les comptes et les paramètres
                                      de la plateforme

  Responsable du projet               Vérifier que le produit répond aux
                                      objectifs

  Développeur                         Comprendre ce qu'il doit construire

  Testeur QA                          Vérifier que le comportement
                                      correspond aux exigences
  -----------------------------------------------------------------------

Les utilisateurs et les parties prenantes ne sont donc pas exactement la
même chose.

**Question à se poser :** qui utilise, finance, développe, valide ou
subit les conséquences du logiciel ?

## 4. Définir le périmètre (*Define the scope*)

Le *scope* définit ce qui est inclus dans le projet et ce qui n'est pas
inclus.

C'est essentiel pour éviter le *scope creep*, c'est-à-dire l'ajout
progressif de nouvelles fonctionnalités sans réévaluation du temps, du
budget ou des ressources.

Exemple :

**Inclus dans la première version (MVP) :**

-   Consultation des disponibilités.
-   Création d'une réservation.
-   Confirmation.
-   Espace restaurateur pour gérer les réservations.

**Exclu de la première version :**

-   Paiement en ligne.
-   Programme de fidélité.
-   Gestion des livraisons.
-   Application mobile native.

Le MVP (*Minimum Viable Product*) est la première version suffisamment
fonctionnelle pour apporter une valeur réelle et recueillir des retours.

**Question à se poser :** que doit-on absolument livrer dans la première
version, et que peut-on reporter ?

## 5. Définir les contraintes (*Constraints*)

Une contrainte est une limite que le projet doit respecter.

Les contraintes peuvent être :

-   **Temporelles** : le produit doit être livré avant une date précise.
-   **Budgétaires** : le budget disponible est limité.
-   **Techniques** : l'équipe doit utiliser une technologie
    particulière.
-   **Humaines** : l'équipe comporte un seul développeur ou peu de
    spécialistes.
-   **Légales** : le logiciel doit respecter les règles applicables,
    notamment en matière de données personnelles.
-   **Opérationnelles** : l'application doit fonctionner sur les
    navigateurs et appareils ciblés.

Exemple : le projet doit être développé en MERN, avec un budget
d'hébergement limité et une première version livrable en huit semaines.

Attention : une contrainte est une limite imposée ou convenue. Une
préférence, comme vouloir utiliser React, n'est pas forcément une
contrainte tant que cette décision n'est pas obligatoire.

**Question à se poser :** quelles limites influencent nos décisions ?

## 6. Estimer les ressources (*Estimate the resources*)

Les ressources sont les moyens nécessaires pour réaliser le projet.

On distingue notamment :

-   **Ressources humaines** : développeurs, testeurs, designer, chef de
    projet.
-   **Ressources techniques** : ordinateurs, serveurs, bases de données,
    outils.
-   **Ressources financières** : hébergement, nom de domaine, licences,
    rémunérations.
-   **Temps disponible** : heures de travail et durée du projet.

Exemple : un développeur seul peut réaliser un MVP plus simple qu'une
équipe comprenant un développeur frontend, un développeur backend, un
designer et un testeur.

L'estimation doit tenir compte non seulement du développement, mais
aussi des tests, de la documentation, du déploiement et des corrections.

**Question à se poser :** de quels moyens avons-nous besoin et lesquels
avons-nous déjà ?

## 7. Identifier les risques (*Identify the risks*)

Un risque est un événement incertain qui pourrait avoir un effet négatif
sur le projet. Il peut affecter le budget, le délai, la sécurité, la
qualité ou la réussite commerciale.

Un risque n'est pas la même chose qu'un problème déjà survenu : une fois
qu'il se produit, on parle généralement d'incident ou de problème avéré.

Exemples :

  -----------------------------------------------------------------------
  Risque                  Conséquence possible    Mesure préventive
  ----------------------- ----------------------- -----------------------
  Réservations en double  Mauvaise expérience     Concevoir une gestion
                          client                  fiable des conflits de
                                                  réservation

  Fuite de données        Atteinte à la           Contrôler les accès,
                          confidentialité         protéger les données et
                                                  tester la sécurité

  Retard de développement Livraison tardive       Limiter le MVP et
                                                  prévoir une marge

  Faible adoption         Peu de restaurants      Tester le concept avec
                          utilisent l'application des restaurateurs avant
                                                  d'investir davantage

  Perte de données        Réservations perdues    Prévoir des sauvegardes
                                                  et tester leur
                                                  restauration
  -----------------------------------------------------------------------

Dans certains projets, on évalue chaque risque selon deux critères :

-   **Probabilité** : quelle est la chance qu'il se produise ?
-   **Impact** : quelles seraient les conséquences s'il se produisait ?

On peut ensuite prioriser les risques les plus importants.

**Question à se poser :** qu'est-ce qui pourrait mal se passer, et
comment réduire les conséquences ?

## 8. Définir le planning (*Create the schedule*)

Le planning organise le travail dans le temps.

Il identifie les phases, les tâches, les dépendances et les échéances.

Exemple simplifié :

  Période         Travail
  --------------- -------------------------------------
  Semaine 1       Analyse du besoin et spécifications
  Semaine 2       UX/UI et architecture
  Semaines 3--4   API et base de données
  Semaines 4--5   Interface React et intégration
  Semaines 5--6   Tests, corrections et sécurité
  Semaine 7       Préproduction et recette
  Semaine 8       Déploiement et suivi initial

Dans la réalité, certaines activités peuvent se dérouler en parallèle.
Le planning doit donc tenir compte des dépendances : par exemple,
l'interface peut être développée à partir d'un contrat d'API défini,
sans attendre que tout le backend soit terminé.

**Question à se poser :** dans quel ordre travailler, combien de temps
prévoir et quelles tâches dépendent des autres ?

## 9. Définir le budget (*Estimate the budget*)

Le budget correspond au coût estimé du projet.

Il peut inclure :

-   Le temps de travail des personnes impliquées.
-   L'hébergement et la base de données.
-   Le nom de domaine.
-   Les outils et licences.
-   Les services externes, par exemple l'envoi d'e-mails.
-   La maintenance et les corrections.
-   Une réserve pour les imprévus.

Même pour un projet personnel, il est utile de distinguer le coût
financier réel du temps investi.

**Question à se poser :** combien le projet va-t-il coûter pour être
construit, livré et maintenu ?

## 10. Définir les critères de réussite (*Success criteria*)

Les critères de réussite permettent de déterminer si le projet atteint
ses objectifs.

Ils doivent être vérifiables, et pas simplement subjectifs.

Exemples :

-   Un client peut créer une réservation valide.
-   Une réservation ne peut pas être créée sur un créneau indisponible.
-   Le restaurateur peut consulter ses réservations.
-   Les utilisateurs ne peuvent pas accéder aux données auxquelles ils
    n'ont pas droit.
-   Les parcours critiques réussissent les tests définis.
-   Les performances respectent les objectifs convenus.
-   Les premiers restaurants pilotes utilisent effectivement le service.

Il faut distinguer les critères de réussite du projet des critères
d'acceptation d'une fonctionnalité : les premiers évaluent le résultat
global, les seconds vérifient une fonctionnalité précise.

**Question à se poser :** quelles preuves nous permettront d'affirmer
que le projet est réussi ?

------------------------------------------------------------------------

## Résumé de la phase Planning

À la fin de cette phase, on doit pouvoir répondre clairement à ces dix
questions :

-   [ ] Quel problème résout-on ?
-   [ ] Quels résultats veut-on atteindre ?
-   [ ] Qui sont les utilisateurs et parties prenantes ?
-   [ ] Qu'est-ce qui est inclus ou exclu du projet ?
-   [ ] Quelles sont les contraintes ?
-   [ ] Quelles ressources sont nécessaires ?
-   [ ] Quels sont les principaux risques ?
-   [ ] Quel est le planning prévisionnel ?
-   [ ] Quel est le budget estimé ?
-   [ ] Comment mesurera-t-on la réussite ?

Une fois ces éléments suffisamment définis, le projet peut passer à
l'analyse détaillée des exigences (*Requirements Analysis*). En Agile,
certaines décisions sont affinées progressivement plutôt que toutes
figées dès le départ.

## SDLC --- Phase 2 - Recueillir les besoins

Identifier les attentes du client, des utilisateurs et des autres parties prenantes (*stakeholders*).

Exemple :
- Le client veut permettre aux utilisateurs de réserver une table au restaurant.
- Les utilisateurs veulent trouver un restaurant et réserver facilement.
- Le restaurateur veut gérer les réservations et les disponibilités.

## 3. Définir les exigences fonctionnelles

Décrire **ce que le logiciel doit faire**.

Exemples :
- Un utilisateur peut rechercher un restaurant.
- Un utilisateur peut choisir une date et une heure.
- Le système peut enregistrer une réservation.
- Le restaurateur peut consulter les réservations.

## 4. Définir les exigences non fonctionnelles

Décrire **comment le logiciel doit fonctionner**, notamment ses qualités et ses contraintes.

Exemples :
- Performance : les pages doivent se charger rapidement.
- Sécurité : les données personnelles doivent être protégées.
- Accessibilité : le site doit être utilisable au clavier.
- Compatibilité : le site doit fonctionner sur les navigateurs ciblés.
- Disponibilité : le service doit rester accessible autant que possible.

## 5. Rédiger les User Stories

Décrire un besoin du point de vue de l'utilisateur.

Format courant :

> En tant que [type d'utilisateur], je veux [action] afin de [bénéfice].

Exemple :

> En tant que client, je veux réserver une table en ligne afin de planifier mon repas.

## 6. Définir les critères d'acceptation

Préciser les conditions qui doivent être remplies pour considérer une fonctionnalité comme correcte.

Exemple pour la réservation :
- La date et l'heure doivent être valides.
- Le créneau doit être disponible.
- Les informations obligatoires doivent être renseignées.
- La réservation doit être enregistrée.
- Une confirmation doit être affichée à l'utilisateur.

## 7. Identifier les règles métier

Définir les règles propres au fonctionnement de l'application.

Exemples :
- Une réservation ne peut pas être faite sur un créneau complet.
- Un utilisateur ne peut pas réserver une date passée.
- Le restaurateur peut annuler une réservation.

## 8. Identifier les contraintes et dépendances

Lister les éléments qui peuvent limiter ou influencer le développement.

Exemples :
- Budget et délais imposés.
- Technologies à utiliser.
- Obligations légales, comme le RGPD.
- Dépendances à des API ou services externes.
- Compatibilité avec certains navigateurs ou appareils.

## 9. Vérifier et valider les exigences

S'assurer que les exigences sont :
- **Claires** : elles ne prêtent pas à confusion.
- **Complètes** : les informations nécessaires sont présentes.
- **Cohérentes** : elles ne se contredisent pas.
- **Testables** : il est possible de vérifier leur respect.
- **Traçables** : elles peuvent être reliées aux tests correspondants.

## 10. Livrables de cette phase

À la fin de l'analyse, on peut disposer de :
- Un document de spécifications (*requirements specification*).
- Une liste d'exigences fonctionnelles et non fonctionnelles.
- Un ensemble de user stories.
- Des critères d'acceptation.
- Des règles métier.
- Une liste de contraintes et de dépendances.
- Des exigences prêtes à être priorisées et planifiées.

---

## Le rôle du testeur QA

Le testeur peut intervenir dès cette phase pour :
- Repérer les exigences ambiguës ou manquantes.
- Vérifier que les exigences sont testables.
- Identifier les cas limites et les erreurs possibles.
- Poser des questions sur les comportements attendus.
- Préparer les futurs scénarios de test.

**Exemple :** que doit-il se passer si deux clients tentent de réserver la dernière table disponible au même moment ?

---

## À ne pas confondre

| Élément | Rôle | Exemple |
|---|---|---|
| Besoin | Exprime une attente | Réserver facilement une table |
| Exigence | Définit ce que le logiciel doit faire | Le système doit permettre de réserver un créneau disponible |
| User story | Présente le besoin du point de vue utilisateur | En tant que client, je veux réserver une table |
| Critère d'acceptation | Définit les conditions de réussite | Une réservation valide doit être enregistrée |
| Cas de test | Décrit comment vérifier le comportement | Réserver un créneau disponible et vérifier la confirmation |

## Checklist

- [ ] Identifier les utilisateurs et les parties prenantes.
- [ ] Recueillir les besoins.
- [ ] Définir les exigences fonctionnelles.
- [ ] Définir les exigences non fonctionnelles.
- [ ] Rédiger les user stories.
- [ ] Définir les critères d'acceptation.
- [ ] Identifier les règles métier.
- [ ] Recenser les contraintes et dépendances.
- [ ] Vérifier que les exigences sont claires et testables.
- [ ] Faire valider les exigences avant de poursuivre.

## SDLC — Phase 3 : Design (Conception)

## 1. Objectif

Définir comment le logiciel sera construit à partir des exigences établies lors de la phase d'analyse.

Cette phase transforme **ce que le logiciel doit faire** en une conception technique et visuelle qui guidera le développement.

## 2. Concevoir l'architecture technique

Définir les grandes parties du système et la manière dont elles communiquent.

Exemples :
- Frontend : interface utilisée par les utilisateurs.
- Backend : logique métier et traitement des requêtes.
- Base de données : stockage des informations.
- API : communication entre le frontend et le backend.
- Services externes : paiement, géolocalisation, notifications, etc.

Exemple pour une application de réservation :
- React pour le frontend.
- Node.js et Express pour le backend.
- MongoDB pour la base de données.
- API REST pour les échanges entre frontend et backend.

## 3. Concevoir la base de données

Définir les données à stocker, leur structure et leurs relations.

Exemple :
- Users : utilisateurs.
- Restaurants : restaurants.
- Reservations : réservations.
- Availability : disponibilités.

Déterminer :
- Les champs de chaque entité.
- Les types de données.
- Les relations entre les données.
- Les contraintes d'intégrité.
- Les index nécessaires aux recherches.
- Les règles de validation.

## 4. Concevoir l'API

Définir comment les différentes parties du logiciel échangeront des données.

Pour une API REST, préciser :
- Les endpoints.
- Les méthodes HTTP.
- Les paramètres et les données attendues.
- Les réponses renvoyées.
- Les codes de statut HTTP.
- L'authentification et les autorisations.
- La gestion des erreurs.

Exemples :
- `GET /restaurants` : récupérer les restaurants.
- `GET /restaurants/:id` : consulter un restaurant.
- `POST /reservations` : créer une réservation.
- `DELETE /reservations/:id` : annuler une réservation.

## 5. Concevoir l'UX/UI

Définir l'expérience utilisateur et l'apparence de l'interface.

### UX — User Experience

L'UX concerne la facilité avec laquelle l'utilisateur accomplit ses tâches.

Exemples :
- Organiser le parcours de réservation.
- Réduire le nombre d'étapes.
- Prévoir les messages d'erreur.
- Faciliter la navigation.

### UI — User Interface

L'UI concerne les éléments visuels et interactifs.

Exemples :
- Couleurs et typographie.
- Boutons et formulaires.
- Mise en page.
- Menus et composants.
- Adaptation aux mobiles et aux ordinateurs.

Livrables possibles :
- Wireframes : maquettes simplifiées.
- Maquettes graphiques : apparence détaillée des écrans.
- Prototypes : versions interactives permettant de tester les parcours.

## 6. Définir la sécurité

Prévoir la protection des données et des fonctionnalités dès la conception.

Exemples :
- Authentification des utilisateurs.
- Contrôle des autorisations côté serveur.
- Validation des données reçues.
- Protection contre les injections et les attaques courantes.
- Gestion sécurisée des mots de passe et des secrets.
- Limitation des requêtes abusives.
- Protection des données personnelles.

La sécurité ne doit pas reposer uniquement sur le frontend : les contrôles essentiels doivent aussi être réalisés côté serveur.

## 7. Définir les choix techniques

Sélectionner les technologies, bibliothèques et outils adaptés au projet.

Exemples :
- Langages et frameworks.
- Base de données.
- Outils de test.
- Gestion de versions avec Git.
- Environnements de développement et de production.
- CI/CD et hébergement.

Les choix doivent tenir compte des besoins, des compétences disponibles, du budget, de la maintenance et de la sécurité.

## 8. Préparer la stratégie de test

Anticiper la manière dont le logiciel sera vérifié.

Exemples :
- Tests unitaires : vérifier une fonction isolément.
- Tests d'intégration : vérifier les échanges entre composants.
- Tests end-to-end (E2E) : vérifier un parcours complet.
- Tests de sécurité.
- Tests de performance.
- Tests d'accessibilité.

Le testeur QA peut examiner la conception pour détecter les risques et préparer les futurs cas de test.

## 9. Livrables de cette phase

Selon le projet, la phase de conception peut produire :
- Un schéma d'architecture.
- Un modèle de données.
- Une spécification de l'API.
- Des wireframes et des maquettes UI.
- Un prototype interactif.
- Des décisions techniques documentées.
- Des règles de sécurité.
- Une stratégie de test initiale.

## 10. Checklist

- [ ] Définir l'architecture technique.
- [ ] Définir les composants frontend et backend.
- [ ] Concevoir le modèle de données.
- [ ] Définir les endpoints de l'API.
- [ ] Concevoir les parcours UX.
- [ ] Créer les maquettes UI nécessaires.
- [ ] Définir les choix technologiques.
- [ ] Prévoir les mesures de sécurité.
- [ ] Anticiper les tests.
- [ ] Vérifier que la conception répond aux exigences.

---

## À ne pas confondre

| Élément | Rôle | Exemple |
|---|---|---|
| Requirements Analysis | Définit ce que le logiciel doit faire | Le client peut réserver une table |
| Design | Définit comment le logiciel sera conçu | Un formulaire React envoie une requête à une API Express |
| Development | Construit le logiciel | Programmer le formulaire et l'endpoint |
| Testing | Vérifie le comportement réel | Vérifier qu'une réservation valide est enregistrée |

**À retenir :** la conception sert de plan de construction. Elle réduit les ambiguïtés et les erreurs avant que le développement ne commence.
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

## 4. Les niveaux de test (Test Levels )

Un **niveau de test** (_test level_) représente un ensemble d’activités de test organisé autour d’un objectif et d’un périmètre particuliers. Les niveaux aident à structurer les tests, mais leur organisation exacte dépend du projet.

### Test des composants (Component Testing / ?Unit Tests?)

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
