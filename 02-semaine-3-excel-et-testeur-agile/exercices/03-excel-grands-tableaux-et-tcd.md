# Exercice 03 — Grands tableaux et tableau croisé dynamique

## Objectif

Nettoyer, filtrer et résumer un tableau de résultats de test avec un tableau croisé dynamique (TCD).

## Mise en situation

Une équipe a consigné les résultats d’une campagne sur plusieurs fonctionnalités. Saisis les données dans Excel sous forme de tableau structuré :

| ID | Fonctionnalité | Environnement | Statut | Priorité |
| --- | --- | --- | --- | --- |
| T-101 | Connexion | Chrome | Réussi | Haute |
| T-102 | Connexion | Firefox | Échoué | Haute |
| T-103 | Recherche | Chrome | Réussi | Moyenne |
| T-104 | Recherche | Firefox | Bloqué | Moyenne |
| T-105 | Panier | Chrome | Échoué | Haute |
| T-106 | Panier | Firefox | Réussi | Haute |
| T-107 | Paiement | Chrome | Bloqué | Haute |
| T-108 | Paiement | Firefox | Échoué | Haute |
| T-109 | Profil | Chrome | Réussi | Basse |
| T-110 | Profil | Firefox | Réussi | Basse |
| T-111 | Recherche | Chrome | À exécuter | Moyenne |
| T-112 | Panier | Chrome | Réussi | Moyenne |

## Travail demandé

### 1. Vérifier la qualité du tableau

- Vérifie les en-têtes et les types de données.
- Recherche les lignes ou cellules vides, doublons d’ID, espaces superflus et statuts écrits de façon incohérente.
- Ajoute un enregistrement supplémentaire et vérifie que le tableau structuré s’étend.
- Trie par fonctionnalité, puis par statut, sans séparer les valeurs d’une même ligne.

### 2. Filtrer les données

- Affiche seulement les tests de priorité haute.
- Affiche ensuite seulement les tests échoués ou bloqués.
- Note le nombre de résultats visibles et vérifie que les filtres actifs sont faciles à repérer.

### 3. Créer un tableau croisé dynamique

Crée un TCD qui affiche le nombre d’ID de test par fonctionnalité et par statut. Ajoute l’environnement comme filtre ou comme dimension supplémentaire.

Vérifie :

- que la source comprend toutes les lignes ;
- que le champ ID est compté et non additionné ;
- que les statuts sont bien répartis dans les bonnes colonnes ;
- que le TCD est actualisé après l’ajout de la nouvelle ligne.

### 4. Interpréter la synthèse

- Quelle fonctionnalité contient le plus de tests non réussis ?
- Quelle information le TCD ne permet-il pas d’obtenir à elle seule ?
- Quelles vérifications manuelles seraient utiles avant de communiquer les résultats ?

## Auto-évaluation

- Les filtres et les tris conservent l’association entre les colonnes.
- Les doublons et valeurs incohérentes ont été recherchés.
- Le TCD couvre toutes les lignes et compte les tests correctement.
- Le TCD est actualisé après modification de la source.
- L’interprétation tient compte des limites des données agrégées.
