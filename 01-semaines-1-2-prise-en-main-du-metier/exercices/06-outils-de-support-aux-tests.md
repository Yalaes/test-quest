# Exercice 06 — Suivre des tests avec un outil (Exercise 06 — Tracking Tests with a Tool)

## Objectifs (Objectives)

- organiser une campagne de vérifications manuelles sur un site web public ;
- consigner les cas, résultats et observations dans un outil de suivi ;
- relier les informations de l’outil aux concepts étudiés dans les notes 01 à 05 ;
- évaluer l’utilité et les limites des outils employés.

## Préparation (Preparation)

Le support de l’exercice est le site public [methode-reformer.com](https://methode-reformer.com/). Le site indique être en bêta et invite ses visiteurs à signaler des soucis ; cela ne vaut pas autorisation pour des tests intrusifs. L’exercice reste limité à une **navigation manuelle normale sur les pages publiques**. Cet exercice est indépendant et ne constitue ni un audit officiel ni une affiliation avec le propriétaire du site.

N’effectue pas de réservation, d’achat, de création de compte, de connexion ni d’envoi de formulaire ou de message. Ne teste pas la sécurité, la charge, les performances ou les limites du site. Ne lance pas de scan ni de test automatisé. Si un parcours te demande une donnée personnelle ou semble engager une réservation, arrête-toi à cette étape.

Choisis un support de suivi :

- **Local, sans compte (recommandé)** : utilise le [dossier de projet préparé](projet-semaine-1-2-methode-reformer/README.md), qui contient le workflow, le plan, la campagne, la revue statique, le journal d’observations, le rapport et les consignes de captures.
- **GitHub privé** : crée un dépôt privé personnel réservé à l’exercice, consigne les cas dans un fichier Markdown et utilise GitHub Issues pour les observations. N’ouvre pas d’issue publique sur le dépôt du site et ne contacte pas l’entreprise dans le cadre de cet exercice.
- **Outil de gestion de tests déjà fourni** : utilise seulement un espace d’entraînement autorisé. N’achète pas de licence et ne crée pas d’élément dans un espace professionnel sans permission.

Consigne le navigateur, sa version si connue, le système utilisé, la date et les pages visitées. N’enregistre pas de cookies, de coordonnées personnelles ni de captures révélant des données privées. Ce travail est un exercice indépendant, sans affiliation avec Méthode Reformer ni avec son propriétaire ; les observations ne sont pas un audit officiel.

## Workflow de l’exercice (Exercise Workflow)

1. **Préparer le suivi** : créer un fichier local ou un projet privé pour y enregistrer le plan, les cas et les résultats.
2. **Définir le périmètre** : retenir uniquement les pages publiques d’information et la navigation ordinaire entre ces pages.
3. **Préparer les cas** : écrire les étapes et les résultats attendus avant d’ouvrir le site ; prévoir les cas ci-dessous.
4. **Exécuter manuellement** : parcourir le site une fois selon les cas, sans répéter rapidement les actions ni envoyer de données.
5. **Consigner les résultats** : noter `Réussi`, `Échoué`, `Bloqué` ou `Non exécuté`, avec les observations factuelles.
6. **Créer un rapport si nécessaire** : ne rédiger un défaut que si tu as réellement observé un écart reproductible. Sinon, écris `Aucun défaut observé pendant ce parcours` ou fais un exemple fictif clairement étiqueté.
7. **Faire le bilan et la révision** : résumer la couverture et relier les choix aux notes 01 à 05.

## Mise en situation (Scenario)

Le site public présente un studio Pilates Reformer. La navigation comprend notamment l’accueil, le studio, les cours, les formules et tarifs, le coaching sur mesure, la page contact et une FAQ. Un bandeau de consentement aux cookies peut apparaître. Le site indique également être en bêta.

Tu vas vérifier la cohérence de la navigation et des informations visibles, sans évaluer la qualité commerciale ou médicale des contenus et sans entreprendre de réservation. Les pages et contenus pouvant changer, consigne ce que tu observes à la date de l’exercice plutôt que de supposer un résultat à l’avance.

## Exercice 1 — Organiser une campagne de navigation (Organize a Navigation Test Campaign)

Dans ton support de suivi :

Crée quatre cas de test :

| ID        | Vérification                                                                                                                                                                                                                         | Résultat attendu                                                                                                      |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------- |
| TC-WEB-01 | Ouvrir la [page d’accueil](https://methode-reformer.com/) et repérer la navigation principale                                                                                                                                        | La page s’affiche et les liens de navigation sont visibles et compréhensibles.                                        |
| TC-WEB-02 | Suivre les liens publics vers [Le studio](https://methode-reformer.com/le-studio/), [Pilates Reformer](https://methode-reformer.com/pilates-reformer/) et [Nos formules & tarifs](https://methode-reformer.com/nos-formules-tarifs/) | Chaque lien mène à une page correspondante ; noter le titre ou le contenu effectivement affiché.                      |
| TC-WEB-03 | Ouvrir [Contact & accès](https://methode-reformer.com/contact-acces/) et relever les moyens d’accès affichés                                                                                                                         | La page s’ouvre et les informations de contact/localisation sont lisibles ; ne pas appeler ni envoyer de message.     |
| TC-WEB-04 | Revenir à la [FAQ de l’accueil](https://methode-reformer.com/) et ouvrir puis refermer une question, si l’accordéon est interactif                                                                                                   | La réponse apparaît puis se replie ; sinon consigner le comportement observé sans déclarer automatiquement un défaut. |

Pour chaque cas, ajoute les préconditions, les étapes détaillées, la date, le navigateur et le statut observé. Le résultat attendu sert de point de comparaison : ne transforme pas une préférence esthétique en défaut sans critère convenu.

Si le bandeau cookies s’affiche, tu peux observer qu’il apparaît et choisir « Tout rejeter » si cette option est proposée. Ne sélectionne pas « Tout accepter » uniquement pour l’exercice. Note le comportement sans tenter d’inspecter ou de modifier les cookies du site.

## Exercice 2 — Enregistrer une observation (Record an Observation)

Dans ton fichier local, GitHub Issue privé ou outil de formation autorisé :

- consigne une anomalie uniquement si tu as observé un écart clair entre un résultat attendu et le résultat réel ;
- indique le cas associé, l’URL publique visitée, la date et la configuration réelle ;
- décris les étapes de reproduction, le résultat attendu et le résultat observé ;
- joins une capture seulement si elle ne contient aucune donnée personnelle ; sinon, décris le constat par écrit ;
- distingue la sévérité de l’impact et la priorité de traitement, en justifiant les deux ;
- ne crée pas d’issue sur le dépôt du site, ne contacte pas son propriétaire et ne publie pas de rapport public. Pour cet exercice, garde le suivi dans ton espace privé ou local.

Si aucun défaut n’est observé, n’en invente pas un. Note `Aucun défaut reproductible observé` et explique qu’un passage de test limité ne prouve pas l’absence de défauts. Tu peux ajouter un exemple de rapport fictif, mais marque-le clairement comme tel.

## Exercice 3 — Réviser les concepts avec les outils (Review Concepts Through the Tools)

À partir des artefacts créés et de la situation :

### Principes fondamentaux — Note 01

- Quel principe explique pourquoi quatre cas de test ne prouvent pas l’absence de défauts ?
- Distingue l’erreur humaine éventuelle, le défaut observé dans le produit et la défaillance visible par le client.

### Cycle de vie et niveaux — Note 02

- Quel niveau de test correspond à vérifier de bout en bout la navigation entre l’accueil et les pages publiques sélectionnées ?
- Quelle interaction entre éléments du site peux-tu vérifier sans dépasser le périmètre autorisé (par exemple un lien de navigation qui ouvre sa page cible) ?
- Si une page ou le menu change, quels tests de régression manuels rejouerais-tu ?

### Techniques statiques — Note 03

- Propose un document ou une exigence à relire avant l’exécution des tests et un problème que cette revue pourrait révéler.
- Quelle différence y a-t-il entre une revue humaine et une analyse statique effectuée par un outil ?

### Techniques de conception — Note 04

- Regroupe les liens observés en classes d’équivalence selon leur destination (navigation interne, contact par courriel/téléphone, autre destination) et explique ce qui est vérifié pour chaque classe.
- Choisis une valeur ou un cas limite pertinent pour la navigation ou l’affichage (par exemple une entrée de menu longue ou une page ayant plusieurs liens vers la même destination) et précise le résultat attendu.
- Quelle technique de conception utiliserais-tu pour vérifier plusieurs conditions combinées, et dans quel autre exemple de test elle serait plus adaptée que dans ce parcours exploratoire ?

### Gestion des tests — Note 05

- Quel risque produit pourrait affecter le plus les visiteurs (par exemple une information de tarif incohérente ou un lien de contact inopérant) ? Justifie sans supposer qu’un défaut existe.
- Quelles informations l’équipe doit-elle suivre pour rendre le résultat de cette campagne limitée compréhensible ?
- Quelles informations de configuration faut-il conserver pour reproduire une anomalie observée ?
- Quels critères de sortie proposerais-tu pour cette campagne de navigation ?

## Exercice 4 — Évaluer le choix d’outils (Evaluate the Tool Choice)

À partir de ton expérience avec l’outil de gestion et de suivi :

- quelle activité l’outil a-t-il facilitée ?
- quelle information a été difficile à saisir, retrouver ou relier ?
- quelles fonctions nécessiteraient une configuration, une licence ou une intégration ?
- quelles données ne faudrait-il pas y stocker ?
- l’outil est-il adapté à une équipe débutante, à un petit projet ou à une grande équipe ? Justifie avec un critère concret.
- nomme une activité de gestion ou d’analyse de test qui doit rester humaine même si des outils sont utilisés.

## Réponse à compléter (Answer Template)

### Outil de gestion choisi (Selected Test Management Tool)

- Parcours choisi (GitHub, outil de formation, local) :
- Nom de l’outil et édition, si connue :
- Dépôt privé, espace autorisé ou dossier local utilisé :
- Plan ou regroupement créé :
- Suite ou cycle créé :
- Nombre de cas de test créés :
- Liens entre cas et pages ou besoins observés :
- Résultats enregistrés :
- Résultats réellement observés ou simulés :
- Rapport ou vue d’avancement consulté :
- Observation et limites du rapport :

### Cas de test créé (Example Test Case)

- Identifiant et titre :
- Objectif :
- Préconditions :
- Page ou URL publique visitée :
- Configuration :
- Étapes :
  1.
  2.
  3.
- Résultat attendu :
- Résultat obtenu ou statut d’exercice :

### Rapport de défaut (Defect Report)

- Outil utilisé :
- Titre :
- Page ou URL publique concernée :
- Version du site si affichée, sinon « inconnue » :
- Date, navigateur et configuration réellement utilisés :
- Étapes de reproduction :
  1.
  2.
  3.
- Résultat attendu :
- Résultat observé :
- Preuves utiles (sans données privées) :
- Sévérité et justification :
- Priorité et justification :
- Lien vers le cas de test :
- État du défaut avant retest :

### Révision des concepts (Concept Review)

- Note 01 — principe mobilisé et distinction erreur/défaut/défaillance :
- Note 02 — niveau, intégration/navigation et régression :
- Note 03 — revue ou analyse statique :
- Note 04 — classes d’équivalence, cas limites et technique de conception :
- Note 05 — risques, suivi, configuration observée et critères de sortie :

### Évaluation de l’outil (Tool Evaluation)

- Point fort observé :
- Limite observée :
- Coût, accès ou intégration à vérifier :
- Données à protéger :
- Activité nécessitant toujours un jugement humain :

## Ressources utiles (Useful Resources)

- [Créer un dépôt GitHub](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository) : créer le dépôt privé d’exercice.
- [Démarrage avec GitHub Issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/quickstart) : prérequis, création et suivi d’une issue.
- [À propos de GitHub Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects) : vues tableau, Kanban et chronologie pour organiser les issues et tâches.

## Auto-évaluation (Self-Assessment)

Avant de considérer l’exercice terminé, vérifier que :

- un plan, une suite ou un regroupement et plusieurs cas ont été consignés dans l’outil ou les fichiers choisis ;
- chaque cas contient des étapes et un résultat attendu suffisamment clairs ;
- les données utilisées sont fictives et toute configuration inconnue est laissée comme inconnue ;
- les résultats réels et simulés sont distingués ;
- aucune exécution fictive n’est présentée comme une observation réelle ;
- seules des pages et interactions publiques et non transactionnelles ont été testées ;
- aucun formulaire, réservation, achat, compte, mécanisme de sécurité ou test de charge n’a été sollicité ;
- le défaut est relié à un test et son rapport est reproductible ;
- sévérité, priorité, retest et régression ne sont pas confondus ;
- les réponses mobilisent des notions de chacune des notes 01 à 05 ;
- les avantages et limites de l’outil sont évalués en tenant compte du contexte.

_N’envoie pas de capture d’écran contenant des noms, adresses, identifiants ou données privées. Tu peux partager tes réponses et les noms des champs utilisés pour obtenir une correction argumentée._
