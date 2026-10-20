# Campagne de test manuel — Méthode Reformer

## Informations de campagne

- Identifiant : CAMP-WEB-01
- Objectif : vérifier quelques parcours de navigation et contenus publics.
- Date d’exécution : à compléter.
- Environnement : compléter les informations dans `plan-de-test.md`.
- Exécutant : à compléter.

## Statuts

- `Réussi` : résultat observé conforme à l’attendu.
- `Échoué` : écart clair, observé et reproductible.
- `Bloqué` : obstacle empêchant l’exécution.
- `Non exécuté` : cas volontairement non exécuté.

Ne marque pas un cas Échoué simplement parce que tu préfères une autre présentation. Décris l’écart factuel et la preuve dans `observations.md`.

## Cas de test

### TC-WEB-01 — Accéder à l’accueil et repérer le menu

- Priorité : moyenne
- Préconditions : navigateur ouvert ; aucune connexion requise.
- Étapes :
  1. Ouvrir https://methode-reformer.com/.
  2. Repérer les entrées visibles du menu principal.
  3. Noter si un bandeau de consentement s’affiche, sans accepter les cookies pour les besoins de l’exercice.
- Résultat attendu : la page d’accueil s’affiche et les entrées principales sont visibles et identifiables.
- Statut : à exécuter.
- Résultat observé :
- Observation / identifiant associé :

### TC-WEB-02 — Suivre les liens vers les pages d’information

- Priorité : moyenne
- Préconditions : TC-WEB-01 exécuté ; rester sur les pages publiques.
- Étapes :
  1. Ouvrir le lien « Le studio » et vérifier le titre ou le sujet de la page.
  2. Revenir à l’accueil ou au menu.
  3. Ouvrir « Pilates Reformer » puis « Nos formules & tarifs ».
  4. Relever la destination réellement atteinte pour chacun.
- Résultat attendu : chaque lien mène à une page dont le titre ou le contenu correspond au libellé annoncé.
- Statut : à exécuter.
- Résultat observé :
- Observation / identifiant associé :

### TC-WEB-03 — Consulter Contact & accès

- Priorité : moyenne
- Préconditions : aucune connexion requise.
- Étapes :
  1. Ouvrir https://methode-reformer.com/contact-acces/ depuis la navigation publique.
  2. Relever les moyens d’accès et informations affichées.
  3. Vérifier que le texte est lisible à l’écran utilisé.
  4. Ne pas appeler, envoyer de courriel ni soumettre de formulaire.
- Résultat attendu : la page s’ouvre et les informations de contact et d’accès sont visibles.
- Statut : à exécuter.
- Résultat observé :
- Observation / identifiant associé :

### TC-WEB-04 — Interagir avec une question de FAQ

- Priorité : basse
- Préconditions : une FAQ ou un accordéon est visible sur une page publique.
- Étapes :
  1. Repérer une question affichée comme ouvrable.
  2. Cliquer une fois sur la question.
  3. Vérifier si une réponse apparaît.
  4. Cliquer à nouveau si le contrôle semble permettre de refermer la réponse.
- Résultat attendu : si l’élément est interactif, la réponse correspondante apparaît et son état peut être compris. Si aucune interaction n’est proposée, noter le cas comme Non exécuté ou Bloqué selon la situation, sans supposer un défaut.
- Statut : à exécuter.
- Résultat observé :
- Observation / identifiant associé :

## Résumé d’exécution

| Statut      | Nombre |
| ----------- | -----: |
| Réussi      |        |
| Échoué      |        |
| Bloqué      |        |
| Non exécuté |        |
| Total       |      4 |

Vérifier que la somme des statuts correspond au total des cas. Compléter après l’exécution.
