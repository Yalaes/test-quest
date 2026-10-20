# Projet d’exercice — Tests du site Méthode Reformer

## Présentation

Ce dossier sert à préparer et consigner un exercice pédagogique de vérification manuelle et de revue statique des pages publiques de [methode-reformer.com](https://methode-reformer.com/). Il n’est pas affilié au propriétaire du site et ne constitue pas un audit officiel.

Le site est en bêta et peut évoluer. Les résultats ci-dessous doivent décrire ce qui a réellement été observé, à la date et dans l’environnement consignés. Ne fabrique pas de défaut pour remplir le rapport.

## Périmètre et règles

L’exercice se limite à une navigation manuelle ordinaire sur des pages accessibles sans compte.

Ne pas :

- réserver, acheter, créer un compte ou se connecter ;
- soumettre un formulaire, envoyer un message, appeler ou effectuer toute action qui contacte le propriétaire ;
- tester la sécurité, les performances, la charge ou les limites du site ;
- lancer de scan, script ou test automatisé ;
- saisir ou conserver des données personnelles, des identifiants ou des informations confidentielles.

Si une action semble déclencher une réservation, un paiement, la création de compte ou l’envoi d’informations, arrêter le parcours et noter le cas comme bloqué ou non exécuté.

## Contenu du dossier

## Index de travail

Lis et utilise les éléments dans cet ordre :

1. [Plan de test](plan-de-test.md) — définir le but, le périmètre, les risques, les limites et l’environnement avant d’ouvrir le site.
2. [Campagne de test manuel](campagne-methode-reformer.md) — parcourir les cas de navigation publics et inscrire le résultat de chaque cas.
3. [Revue statique des pages](revue-statique-methode-reformer.md) — examiner les textes et informations visibles ; cette revue peut se faire en parallèle de la campagne, mais consigne ses constats séparément.
4. [Journal des observations](observations.md) — ajouter au fil de l’eau toute question, anomalie candidate ou limite rencontrée, puis relier chaque entrée au cas ou point de revue concerné.
5. [Captures d’écran](preuves/captures-ecran/README.md) — consulter les règles avant de prendre une preuve ; ne garder que des captures expurgées et utiles.
6. [Rapport de test](rapport-de-test.md) — terminer par une synthèse des résultats réellement obtenus, de la couverture et des limites.

Le fichier [`.gitignore`](.gitignore) protège le dépôt contre l’ajout accidentel de fichiers temporaires et de captures brutes ; il n’est pas une étape de test.

### Workflow rapide

`plan-de-test.md` → `campagne-methode-reformer.md` et `revue-statique-methode-reformer.md` → `observations.md` et preuves expurgées si besoin → `rapport-de-test.md`.

## Workflow conseillé

1. Lire les limites du périmètre et compléter `plan-de-test.md` avant d’ouvrir le site.
2. Noter la date, l’heure approximative, le système, le navigateur et sa version si disponible.
3. Parcourir une fois chaque cas de `campagne-methode-reformer.md` sans multiplier les requêtes.
4. Réaliser séparément la revue de `revue-statique-methode-reformer.md` à partir des seules informations visibles publiquement.
5. Reporter dans `observations.md` uniquement des faits reproductibles ou des questions. Distinguer explicitement une anomalie confirmée d’une hypothèse.
6. Si une capture est utile, la vérifier et la masquer avant conservation. Placer les captures brutes dans `preuves/captures-ecran/brutes/` : ce sous-dossier est ignoré par Git. Ne conserver dans `preuves/captures-ecran/` que des copies expurgées et utiles.
7. Compléter `rapport-de-test.md`, y compris les cas non exécutés et les limites. « Aucun défaut observé » ne signifie pas « absence de défauts ».
8. Relire les fichiers pour retirer toute donnée personnelle ou sensible avant de partager le dossier.

## Résultats et statuts

Utiliser de façon cohérente :

- `Réussi` : le résultat observé correspond au résultat attendu ;
- `Échoué` : un écart clair et reproductible a été constaté ;
- `Bloqué` : le cas n’a pas pu être exécuté en raison d’un obstacle ;
- `Non exécuté` : le cas a été volontairement laissé de côté.

Pour chaque statut, préciser si le résultat vient d’une observation réelle ou d’un exercice simulé. Dans ce projet, les cas de la campagne sont conçus pour être parcourus sur le site public ; ne marque `Échoué` qu’après avoir vérifié et consigné l’écart.
