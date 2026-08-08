---
type: chapitre
id: C06
partie: 2
version: v0.2
status: draft
updated: 2026-08-08
claims_reviewed: partial
source_ids: [SRC-SEI-TD-001, SRC-SEI-ETD-001]
tags: [dette-organisationnelle, gouvernance, complexite, transformation]
---
# C06 · La dette organisationnelle

La dette technique possède une définition relativement claire : un choix de conception ou de construction peut accélérer l'action à court terme tout en augmentant le coût ou la complexité futurs.

Cette idée peut être étendue, avec prudence, à l'organisation elle-même.

Nous appellerons **dette organisationnelle** l'ensemble des décisions, règles, contournements, répartitions de responsabilités et pratiques qui ont permis à l'organisation de fonctionner à un moment donné mais qui augmentent ensuite le coût de compréhension, de coordination ou de transformation.

Ce terme est une proposition du livre.

Il ne doit pas être confondu avec la dette technique.

## Une dette peut être rationnelle

Une dette n'est pas nécessairement une erreur.

Lorsqu'une organisation doit répondre rapidement à une urgence, respecter une échéance réglementaire, lancer un produit ou maintenir un service essentiel, une solution provisoire peut être parfaitement rationnelle.

Le problème apparaît lorsque le provisoire devient permanent sans être requalifié.

La dette commence alors à porter des intérêts.

Ces intérêts ne sont pas seulement financiers.

Ils prennent la forme de :

- temps de coordination ;
- double saisie ;
- validations supplémentaires ;
- dépendance à quelques personnes ;
- difficulté de remplacement d'un outil ;
- réunions de clarification ;
- erreurs répétées ;
- perte de contexte ;
- impossibilité d'expliquer pourquoi une règle existe encore.

## Quand l'organisation oublie la raison de ses propres règles

Une procédure peut survivre à la situation qui l'avait justifiée.

Un tableau de suivi peut continuer à être alimenté après la disparition de son usage réel.

Une validation peut rester obligatoire parce qu'un incident ancien a conduit à ajouter un contrôle.

Un rôle peut conserver un pouvoir alors que le processus a changé.

La dette organisationnelle apparaît lorsque la règle reste visible mais que sa **raison** disparaît.

Ce phénomène transforme la mémoire en contrainte.

Le système conserve la décision mais perd son contexte.

Il devient alors difficile de distinguer une règle essentielle d'un vestige historique.

## Dette locale et dette systémique

Le Software Engineering Institute montre que certaines dettes techniques dépassent le périmètre d'un système isolé et produisent des effets à l'échelle de l'entreprise.

Cette distinction est utile pour notre modèle.

Une dette organisationnelle peut être locale : une équipe maintient deux outils redondants.

Elle devient systémique lorsque plusieurs équipes dépendent de ce doublon, lorsque les données divergent, lorsque les contrats s'entrecroisent ou lorsque la suppression d'un composant nécessite plusieurs arbitrages institutionnels.

La gouvernance doit donc regarder non seulement la dette elle-même, mais son **rayon d'impact**.

## Le coût de compréhension

Nous proposons un indicateur conceptuel simple :

> **une organisation s'endette lorsque le coût nécessaire pour comprendre son fonctionnement augmente plus vite que la valeur produite par sa complexité.**

Cette formulation n'est pas encore une équation opérationnelle.

Elle donne toutefois une direction de mesure.

On pourrait observer :

- temps nécessaire pour retrouver le propriétaire d'une décision ;
- nombre de systèmes traversés pour réaliser une tâche ;
- nombre de validations nécessaires ;
- proportion de procédures dont la justification est documentée ;
- dépendance à des personnes uniques ;
- délai nécessaire pour modifier une règle ;
- quantité de travail manuel servant uniquement à relier des systèmes.

Le but ne serait pas de créer un score universel.

Il serait de rendre visible l'endroit où la complexité cesse d'être productive.

## La dette de connaissance

Une part importante de la dette organisationnelle n'est pas inscrite dans le logiciel.

Elle existe dans la tête des personnes.

Une organisation peut sembler stable parce que quelques individus savent :

- qui appeler ;
- quelle procédure contourner ;
- quel fichier fait foi ;
- quel export corriger ;
- quelle règle n'est plus réellement appliquée ;
- quelle décision n'a jamais été documentée.

Ce savoir tacite possède une valeur immense.

Le considérer uniquement comme un risque serait une erreur.

Il devient une dette lorsqu'il est indispensable mais impossible à transmettre.

La transformation doit donc chercher à **capitaliser sans déposséder** les personnes de leur expertise.

Documenter n'est pas aspirer leur métier.

C'est rendre transmissible ce qui doit survivre.

## La dette de gouvernance

Une organisation peut aussi accumuler une dette de gouvernance.

Les droits ne correspondent plus aux responsabilités réelles.

Les instances de décision se superposent.

Personne ne sait qui peut autoriser une modification.

Les arbitrages sont repoussés parce que les conséquences traversent plusieurs directions.

La dette devient alors politique et organisationnelle.

Un changement technique ne peut plus la résoudre seul.

## Une dette doit être enregistrée, pas seulement ressentie

La dette reste dangereuse lorsqu'elle n'existe que sous forme de plaintes diffuses.

Le SEI recommande de créer des inventaires de dettes techniques et d'en documenter les conséquences.

Nous étendons cette logique au SIIAOS.

Une dette organisationnelle candidate pourrait être décrite ainsi :

```yaml
debt_id: DET-ORG-001
contexte:
raison_historique:
capacites_affectees: []
consequences: []
cout_actuel:
risque_si_inaction:
proprietaire:
options: []
preuve_ids: []
statut:
```

L'objectif n'est pas de bureaucratiser chaque imperfection.

Il est de pouvoir distinguer les tensions structurelles des simples irritants.

## Hypothèse de travail

> **La dette organisationnelle n'est pas la somme des défauts d'une organisation. C'est la somme des arbitrages historiques dont les coûts futurs ne sont plus explicitement gouvernés.**

Cette définition devra être confrontée aux travaux sur routines organisationnelles, path dependence, knowledge management et bureaucratie.

## Transition

Une dette devient particulièrement difficile à voir lorsque l'information nécessaire à sa compréhension est répartie dans plusieurs endroits.

C'est le problème de la [[C07_Fragmentation|fragmentation]].

## Statut des affirmations

**Faits sourcés** : définition et gestion de la dette technique ; existence de dettes techniques à portée d'entreprise nécessitant une gouvernance dépassant l'équipe ou le projet.

**Doctrine** : dette organisationnelle, dette de connaissance, dette de gouvernance.

**Observation de terrain** : survivance de procédures, dépendances à des personnes-clés, difficulté à retrouver la justification historique d'une règle.

**À approfondir** : littérature sur path dependence, organizational routines, bureaucratic burden et knowledge loss.
