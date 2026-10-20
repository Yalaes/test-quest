# Excel — Formules, fonctions et graphiques

## Objectifs

- écrire et recopier des formules ;
- distinguer références relatives, absolues et mixtes ;
- utiliser des fonctions adaptées à une question ;
- choisir un graphique lisible pour présenter des résultats.

## 1. Références de cellules

À compléter avec les exemples vus en cours :

- **relative** : la référence s’ajuste lorsque la formule est copiée ;
- **absolue** : la colonne et la ligne restent fixes ;
- **mixte** : seule la colonne ou la ligne reste fixe.

Exemples de notation : `A1`, `$A$1`, `$A1`, `A$1`.

## 2. Fonctions

Une fonction est une formule prédéfinie. Sa syntaxe générale est :

```excel
=NOM_FONCTION(argument1;argument2)
```

Selon la langue et la version d’Excel, les noms de fonctions et les séparateurs peuvent varier. Noter les fonctions réellement utilisées pendant la formation :

| Besoin | Fonction | Exemple de formule |
| --- | --- | --- |
| Calculer un total |  |  |
| Calculer une moyenne |  |  |
| Compter des valeurs |  |  |
| Tester une condition |  |  |
| Rechercher une information |  |  |

Toujours vérifier les cellules incluses dans la plage et le traitement des cellules vides ou des erreurs.

## 3. Graphiques

Le graphique doit répondre à une question précise et représenter correctement les données.

- comparer des catégories : souvent un graphique en barres ou en colonnes ;
- montrer une évolution dans le temps : souvent un graphique en courbes ;
- illustrer une répartition : choisir un graphique adapté et limiter le nombre de catégories.

À vérifier avant de partager un graphique : titre, axes, unités, légende, plage source et lisibilité.

## À retenir

- Le type de référence détermine comment une formule se comporte lorsqu’elle est copiée.
- Une fonction est utile si ses arguments et son résultat sont compris et vérifiés.
- Un graphique met en évidence une information ; il ne corrige pas des données erronées.

## Révision

1. À quoi sert une référence absolue dans une formule recopiée ?
2. Comment vérifier qu’une fonction ne compte que les lignes souhaitées ?
3. Quel graphique choisirais-tu pour suivre le nombre de tests échoués sur plusieurs jours ? Pourquoi ?
4. Quelles informations faut-il vérifier avant de tirer une conclusion d’un graphique ?

<details>
<summary>Correction proposée</summary>

1. Une référence absolue, par exemple `$A$1`, conserve la même cellule lorsque la formule est copiée. Elle est utile lorsqu’un calcul réutilise une constante située dans une cellule fixe.
2. Vérifier les arguments et la plage de la fonction, puis comparer son résultat avec un petit comptage manuel ou un filtre sur les lignes concernées.
3. Un graphique en courbes convient souvent pour montrer l’évolution par jour, à condition que les dates soient ordonnées et que l’axe et l’unité soient clairement indiqués. Un graphique en colonnes peut aussi convenir pour comparer un nombre limité de jours.
4. Vérifier les données source, la plage sélectionnée, les filtres, les catégories, les unités, l’échelle des axes, le titre et la légende.

</details>

## Références et ressources

- [Aide et formation Excel — Microsoft Support](https://support.microsoft.com/excel) : documentation officielle pour approfondir les formules, les fonctions et les graphiques selon la version d’Excel utilisée.
