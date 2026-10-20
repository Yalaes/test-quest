# Plan de test — Méthode Reformer

## 1. Identification

- Projet : exercice pédagogique de vérification manuelle et de revue statique des pages publiques.
- Site testé : https://methode-reformer.com/
- Auteur du plan : à compléter.
- Date de préparation : à compléter.
- Version du site : non communiquée, sauf indication visible sur le site.

## 2. Objectifs

- vérifier que quelques liens publics conduisent aux pages annoncées ;
- vérifier la lisibilité et la cohérence de certaines informations visibles ;
- consigner les résultats de manière reproductible ;
- distinguer les faits observés, les questions et les hypothèses.

## 3. Périmètre

### Inclus

- page d’accueil et navigation principale ;
- pages publiques « Le studio », « Pilates Reformer », « Nos formules & tarifs » et « Contact & accès » ;
- interactions de lecture simples, comme ouvrir et refermer une question de FAQ ;
- revue humaine des textes et informations publiques sélectionnés.

### Exclu

- réservation, achat, création de compte, connexion et envoi de formulaire ;
- appels, courriels ou autres prises de contact ;
- tests de sécurité, de charge, de performance, d’accessibilité formelle ou de compatibilité exhaustive ;
- inspection du code source et audit officiel.

## 4. Approche

- navigation manuelle, une fois par cas, sans génération de trafic inhabituel ;
- revue statique humaine des contenus visibles, sans exécution de code ni accès au back-office ;
- priorité aux liens et aux informations essentielles pour comprendre l’offre et accéder au studio ;
- enregistrement dans `campagne-methode-reformer.md`, `revue-statique-methode-reformer.md` et `observations.md`.

## 5. Risques et limites

| Risque                                                    | Impact possible                           | Mesure de précaution                                                                      |
| --------------------------------------------------------- | ----------------------------------------- | ----------------------------------------------------------------------------------------- |
| Le site évolue pendant l’exercice                         | Les constats peuvent devenir obsolètes    | Noter date et heure approximative de la vérification                                      |
| Une action déclenche une réservation ou un contact        | Interaction non souhaitée avec le service | Ne pas cliquer sur l’action finale ni soumettre de formulaire                             |
| Une capture contient des données personnelles             | Divulgation involontaire                  | Vérifier et masquer avant de conserver ; ignorer les captures brutes avec le `.gitignore` |
| Un défaut est confondu avec une préférence                | Rapport inexact                           | Décrire le fait, l’attendu et la preuve ; marquer les questions comme hypothèses          |
| Une absence de constat est interprétée comme une garantie | Fausse confiance                          | Indiquer les limites et le périmètre non couvert                                          |

## 6. Environnement à consigner

- Date et heure approximative :
- Système d’exploitation :
- Navigateur et version :
- Type d’affichage (ordinateur, tablette ou téléphone) :
- Réseau particulier ou autre condition pertinente :
- Version du site, si affichée :

Ne consigner aucune adresse IP, donnée de compte, identifiant ou information personnelle.

## 7. Critères de sortie

La campagne peut être considérée terminée lorsque :

- chaque cas est marqué Réussi, Échoué, Bloqué ou Non exécuté ;
- tout échec est décrit dans `observations.md` avec assez de détails pour le retrouver ;
- les limites, risques résiduels et cas non exécutés sont indiqués dans `rapport-de-test.md` ;
- les preuves éventuellement conservées ont été expurgées ;
- aucune action hors périmètre n’a été effectuée.
