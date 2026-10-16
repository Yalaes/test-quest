# Exercice 01 — Cycle de vie et niveaux de test (Exercise 01 — Life Cycle and Test Levels)

## Objectif (Objective)

Appliquer les notions de cycle de vie du développement logiciel (_software development life cycle_, **SDLC**), de niveaux de test (_test levels_), de types de test (_test types_), de décalage des tests vers la gauche (_shift-left testing_) et de tests de maintenance (_maintenance testing_).

## Mise en situation (Scenario)

Une équipe développe une boutique en ligne par versions. La boutique permet déjà de consulter des produits, de gérer un panier et de créer un compte.

Dans la prochaine version, l’équipe ajoute le paiement par carte bancaire avec un prestataire externe. La fonctionnalité doit permettre au client de confirmer sa commande, d’obtenir un résultat clair en cas de paiement accepté ou refusé, et de ne pas débiter deux fois le client s’il clique plusieurs fois sur le bouton de paiement.

L’équipe travaille par itérations courtes et souhaite livrer cette fonctionnalité dès qu’elle est prête. Après la mise en production, le prestataire annonce une mise à jour de son interface de programmation (Application Programming Interface, **API**).

## Travail demandé (Tasks)

### 1. Préparer les tests tôt (Plan Tests Early)

Avant que le développement soit terminé :

- note trois questions à poser à la personne responsable du besoin pour clarifier les exigences ;
- propose une activité de test qui pourrait être réalisée avant l’existence du code ;
- explique quel problème cette activité pourrait aider à détecter tôt.

### 2. Identifier les niveaux de test (Identify Test Levels)

Pour chacun des quatre niveaux ci-dessous, propose un exemple de vérification pertinent pour cette fonctionnalité et explique brièvement son objectif :

- test des composants (_component testing_) ;
- test d’intégration (_integration testing_) ;
- test système (_system testing_) ;
- test d’acceptation (_acceptance testing_).

### 3. Distinguer les types de test (Distinguish Test Types)

Propose :

- deux vérifications fonctionnelles (_functional testing_) ;
- deux vérifications non fonctionnelles (_non-functional testing_), en nommant la caractéristique de qualité visée, par exemple la performance (_performance_), la sécurité (_security_) ou la facilité d’utilisation (_usability_).

Pour chacune, indique à quel niveau elle pourrait être réalisée. Un type de test peut être appliqué à différents niveaux selon le périmètre choisi.

### 4. Prévoir les régressions (Plan for Regression Testing)

Après l’ajout du paiement :

- cite deux fonctionnalités existantes qui pourraient être affectées ;
- propose un test de régression (_regression test_) pour chacune ;
- explique pourquoi ces vérifications sont utiles même si ces fonctionnalités n’ont pas été modifiées intentionnellement.

### 5. Anticiper la maintenance (Anticipate Maintenance Testing)

Après la mise en production, le prestataire met à jour son API :

- explique pourquoi ce changement peut déclencher des tests de maintenance ;
- indique ce qu’il faudrait vérifier en priorité ;
- distingue le retest de la fonctionnalité modifiée des tests de régression autour du paiement.

## Réponse à compléter (Answer Template)

### Préparer les tests tôt (Plan Tests Early)

- Questions à clarifier :
  1.
  2.
  3.
- Activité avant le développement :
- Risque ou problème détecté :

### Niveaux de test (Test Levels)

| Niveau (Level)                           | Exemple de vérification (Example Check) | Objectif (Purpose) |
| ---------------------------------------- | --------------------------------------- | ------------------ |
| Test des composants (Component testing)  |                                         |                    |
| Test d’intégration (Integration testing) |                                         |                    |
| Test système (System testing)            |                                         |                    |
| Test d’acceptation (Acceptance testing)  |                                         |                    |

### Types de test (Test Types)

| Vérification (Check) | Type (Type) | Niveau possible (Possible level) |
| -------------------- | ----------- | -------------------------------- |
|                      |             |                                  |
|                      |             |                                  |
|                      |             |                                  |
|                      |             |                                  |

### Régressions (Regression Testing)

- Fonctionnalité existante 1 :
- Test de régression associé :
- Fonctionnalité existante 2 :
- Test de régression associé :
- Pourquoi les exécuter ?

### Maintenance (Maintenance Testing)

- Pourquoi l’évolution de l’API nécessite une analyse de test ?
- Vérifications prioritaires :
- Retest de la fonctionnalité modifiée :
- Tests de régression autour du paiement :

## Auto-évaluation (Self-Assessment)

Avant de considérer l’exercice terminé, vérifier que :

- les niveaux de test sont distingués par leur périmètre et leur objectif ;
- les types de test décrivent ce qui est vérifié, et non le niveau ;
- les exemples sont liés au scénario et assez précis pour être exécutés ;
- le retest et les tests de régression ne sont pas confondus ;
- les priorités sont justifiées par les risques pour le client ou l’entreprise.

_Rédige tes réponses sans consulter de corrigé. Tu peux ensuite me les envoyer pour une correction argumentée._
