# Excel — Prise en main et tableaux

## Objectifs

- reconnaître les principales zones de l’interface Excel ;
- créer, enregistrer et retrouver un classeur ;
- saisir et modifier des données dans les cellules ;
- présenter des données sous forme de tableau ;
- créer des formules simples et comprendre les références de cellules.

## 1. Découverte de l’outil

### Interface et vocabulaire

À compléter pendant le cours : classeur, feuille, ligne, colonne, cellule, plage, barre de formule, ruban et onglets.

### Premières manipulations

Noter les étapes pour :

- créer et enregistrer un classeur ;
- renommer, ajouter et déplacer une feuille ;
- saisir, modifier et effacer une valeur ;
- sélectionner une cellule ou une plage ;
- ajuster la largeur d’une colonne et la hauteur d’une ligne.

## 2. Organiser des données en tableau

Un tableau bien structuré utilise une ligne d’en-tête, une colonne par information et une ligne par enregistrement. Éviter les lignes et colonnes vides à l’intérieur de la plage de données.

À retenir du cours :

- transformer une plage en tableau ;
- choisir un style et activer les filtres ;
- trier les données sans séparer les lignes ;
- ajouter une ligne et vérifier que le tableau s’étend correctement.

## 3. Formules simples

Une formule commence par le signe `=`. Elle peut utiliser des valeurs, des références de cellules, des opérateurs ou des fonctions.

Exemples à tester pendant le cours :

```excel
=A2+B2
=C2-D2
=E2*F2
=G2/H2
```

Noter la différence entre recopier une formule et saisir à nouveau un calcul, ainsi que le comportement des références lorsque la formule est recopiée.

## 4. Mise en forme des données

Garder une mise en forme cohérente avec le contenu : dates en format date, montants en format monétaire, pourcentages en format pourcentage. La mise en forme facilite la lecture, mais ne doit pas remplacer la valeur réelle de la cellule.

Notes du cours :

- formats numériques utilisés ;
- alignement, bordures et couleurs ;
- mise en forme conditionnelle si présentée ;
- erreurs de mise en forme rencontrées et manière de les corriger.

## À retenir

- Une cellule est repérée par sa colonne et sa ligne.
- Une formule permet d’effectuer un calcul réutilisable.
- Un tableau structuré facilite le tri, le filtrage et l’ajout de données.
- Vérifier le type et le format des données avant d’analyser les résultats.

## Révision

1. Quelle différence y a-t-il entre un classeur et une feuille ?
2. Pourquoi faut-il éviter les lignes vides au milieu d’une plage destinée à devenir un tableau ?
3. Que se passe-t-il lorsqu’on recopie une formule vers une autre ligne ?
4. Pourquoi une valeur qui ressemble à une date peut-elle être traitée comme du texte ?

<details>
<summary>Correction proposée</summary>

1. Un classeur est le fichier Excel qui peut contenir plusieurs feuilles. Une feuille est une grille de cellules à l’intérieur du classeur.
2. Une ligne vide peut interrompre la détection de la plage et compliquer le tri, le filtrage ou l’extension du tableau.
3. Les références relatives se décalent selon la nouvelle position. Les références absolues restent fixes ; les références mixtes ne figent que la ligne ou la colonne indiquée par `$`.
4. Excel peut interpréter cette valeur comme du texte si son format ou sa saisie ne correspond pas aux paramètres régionaux ou au format de date attendu. Dans ce cas, les tris et calculs de dates peuvent ne pas fonctionner comme prévu.

</details>

## Références et ressources

- [Aide et formation Excel — Microsoft Support](https://support.microsoft.com/excel) : documentation officielle pour découvrir le classeur, les cellules, les tableaux et les opérations de base.
