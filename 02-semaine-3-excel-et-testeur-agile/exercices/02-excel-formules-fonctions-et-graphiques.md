# Exercice 02 — Formules, fonctions et graphiques Excel

## Objectif

Utiliser des références de cellules, des fonctions et un graphique pour résumer des résultats de tests.

## Mise en situation

Une équipe suit le temps passé sur des cas de test pendant quatre jours. Crée une feuille `Résultats` et saisis ce tableau :

| Jour | Tests exécutés | Tests réussis | Temps passé (h) |
| --- | ---: | ---: | ---: |
| Lundi | 12 | 9 | 3,5 |
| Mardi | 15 | 12 | 4 |
| Mercredi | 10 | 8 | 3 |
| Jeudi | 18 | 15 | 5 |

Dans une cellule séparée, indique un objectif de réussite de 80 %.

## Travail demandé

### 1. Calculer les résultats

Ajoute les colonnes suivantes :

- `Tests non réussis` : tests exécutés moins tests réussis ;
- `Taux de réussite` : tests réussis divisés par tests exécutés ;
- `Temps moyen par test (min)` : temps passé converti en minutes et divisé par le nombre de tests exécutés.

Ajoute une ligne ou une zone de synthèse qui calcule le total des tests exécutés, le total des tests réussis et le taux de réussite global. Le taux global doit être calculé à partir des totaux, et non comme une moyenne simple des pourcentages journaliers.

### 2. Utiliser des références absolues

Ajoute une colonne `Objectif atteint ?` qui compare le taux journalier à la cellule contenant l’objectif de 80 %.

Recopie la formule vers le bas en utilisant une référence absolue pour la cellule de l’objectif. Note la formule et explique pourquoi cette référence doit rester fixe.

### 3. Vérifier les formules

- Vérifie manuellement le taux du lundi et le taux global.
- Modifie temporairement le nombre de tests réussis du mardi et observe quelles cellules se recalculent.
- Vérifie qu’aucun nombre de tests réussis n’est supérieur au nombre de tests exécutés.
- Restaure ensuite la valeur originale.

### 4. Créer un graphique

Crée un graphique comparant, pour chaque jour, les tests réussis et les tests non réussis. Ajoute un titre, une légende et des étiquettes d’axes si elles améliorent la lecture.

## Questions de réflexion

1. Pourquoi le taux global ne doit-il pas nécessairement être la moyenne des taux journaliers ?
2. À quoi sert la référence absolue utilisée pour l’objectif ?
3. Quelle différence y a-t-il entre une valeur manquante et la valeur zéro dans les données ?
4. Quelles vérifications permettent de s’assurer que le graphique représente les bonnes colonnes et lignes ?

## Auto-évaluation

- Les formules utilisent les bonnes plages et se recopient correctement.
- L’objectif reste fixe lorsque la formule est recopiée.
- Le taux global est pondéré par le nombre de tests exécutés.
- Le graphique compare des données pertinentes et comporte un titre compréhensible.
- Les résultats ont été contrôlés par au moins un calcul manuel.
