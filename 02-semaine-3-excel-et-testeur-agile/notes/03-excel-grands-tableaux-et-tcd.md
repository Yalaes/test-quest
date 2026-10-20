# Excel — Grands tableaux et tableaux croisés dynamiques

## Objectifs

- garder un tableau long exploitable ;
- utiliser filtres et tris sans mélanger les enregistrements ;
- repérer les problèmes de qualité des données ;
- comprendre l’objectif d’un tableau croisé dynamique (TCD).

## 1. Gérer des tableaux longs

Bonnes pratiques à noter pendant le cours :

- conserver une seule ligne d’en-têtes ;
- éviter les cellules fusionnées et les lignes vides dans la plage ;
- utiliser des types cohérents par colonne ;
- convertir la plage en tableau structuré si cela convient ;
- filtrer avant d’analyser, en vérifiant que les filtres actifs sont visibles ;
- trier l’ensemble du tableau, pas une colonne isolée ;
- figer les volets si cela facilite la lecture ;
- supprimer les doublons uniquement après avoir défini ce qui constitue un doublon.

## 2. Nettoyage et vérification

Avant une analyse, vérifier :

- valeurs manquantes ou inattendues ;
- doublons ;
- espaces ou différences d’écriture ;
- dates et nombres interprétés comme texte ;
- filtres ou tris précédemment appliqués ;
- totaux ou décomptes qui ne correspondent pas à un contrôle manuel.

## 3. Tableaux croisés dynamiques

Un **tableau croisé dynamique** résume et explore une source tabulaire sans devoir écrire une formule pour chaque regroupement.

Notions à compléter :

- source de données ;
- champs de lignes et de colonnes ;
- valeurs à compter ou agréger ;
- filtres et segments ;
- actualisation après modification de la source.

Exemple de question d’analyse : « Combien de tests sont réussis, échoués ou bloqués par fonctionnalité ? »

Vérifier que la plage source couvre toutes les lignes, que le type de synthèse (somme, compte, moyenne) est approprié et que le TCD est actualisé.

## À retenir

- Un tri incorrect peut associer une valeur à la mauvaise ligne.
- Un tableau croisé dynamique résume les données selon les champs choisis, mais ne vérifie pas leur exactitude.
- Une synthèse n’est interprétable que si les données et les critères de regroupement sont compris.

## Révision

1. Pourquoi ne faut-il pas trier une seule colonne d’un tableau de données ?
2. Quelles vérifications ferais-tu avant de créer un TCD ?
3. Pourquoi un TCD peut-il présenter des résultats corrects sur une source incomplète et conduire quand même à une mauvaise conclusion ?

<details>
<summary>Correction proposée</summary>

1. Trier une seule colonne peut désolidariser les valeurs de leurs autres champs et associer, par exemple, un statut au mauvais identifiant de test. Il faut trier l’ensemble du tableau.
2. Vérifier les en-têtes, les lignes incluses, les valeurs manquantes, les doublons, les types de données et l’absence de lignes vides qui coupent la source. Choisir aussi une synthèse adaptée, comme un compte plutôt qu’une somme pour compter des tests.
3. Le TCD résume les données qu’il reçoit ; il ne sait pas qu’il manque des lignes. Il peut donc calculer correctement sur une source incomplète, mais ne pas représenter toute la campagne.

</details>

## Références et ressources

- [Créer un tableau croisé dynamique pour analyser des données de feuille de calcul — Microsoft Support](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576) : documentation sur la préparation des données, la création et l’actualisation d’un tableau croisé dynamique.
- [Aide et formation Excel — Microsoft Support](https://support.microsoft.com/excel) : ressources générales sur les tableaux, tris et filtres.
