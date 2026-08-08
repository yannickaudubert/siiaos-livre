---
type: chapitre
id: C12
partie: 3
version: v0.2
status: draft
updated: 2026-08-08
claims_reviewed: partial
source_ids: [SRC-NIST-AIRMF-001, SRC-EU-AIACT-001]
tags: [gouvernance, automatisation, controle-humain, responsabilite]
---
# C12 · Automatiser n'est pas gouverner

Automatiser consiste à faire exécuter une opération sans intervention humaine à chaque étape.

Gouverner consiste à déterminer ce qui peut être automatisé, dans quelles limites, avec quels droits, quelles responsabilités, quels contrôles et quelles possibilités d'arrêt.

Les deux notions sont donc liées, mais elles ne sont pas équivalentes.

## Une chaîne de décision explicite

Une architecture gouvernable doit distinguer plusieurs actes qui sont souvent confondus dans une interface unique :

**observer → proposer → décider → autoriser → exécuter → vérifier → rendre compte.**

Un même acteur peut parfois accomplir plusieurs de ces fonctions.

Mais les distinguer conceptuellement permet de savoir où se trouve réellement la responsabilité.

Une IA peut proposer.

Un workflow peut vérifier qu'une règle formelle est satisfaite.

Un responsable peut autoriser.

Un service automatisé peut exécuter.

Un autre composant peut contrôler le résultat.

La qualité de la gouvernance dépend en partie de la clarté de cette chaîne.

## Le contrôle humain ne doit pas être fictif

Placer un bouton « valider » devant une sortie automatisée ne garantit pas un contrôle humain effectif.

Le responsable doit avoir :

- suffisamment d'informations ;
- suffisamment de temps ;
- une compétence adaptée ;
- la possibilité réelle de contredire le système ;
- la possibilité d'empêcher ou d'interrompre l'action ;
- une compréhension suffisante de la portée de sa décision.

L'article 14 du règlement européen sur l'IA formalise précisément, pour les systèmes à haut risque concernés, l'exigence d'un contrôle humain effectif et proportionné au risque, au niveau d'autonomie et au contexte d'utilisation. Le NIST insiste également sur la clarification des rôles humains, des responsabilités et des mécanismes de supervision.

Cette convergence est importante pour notre architecture.

Le contrôle humain doit être conçu comme une **capacité opérationnelle**, pas comme une présence symbolique.

## Droit d'arrêt

Un système gouvernable doit posséder un chemin d'arrêt.

Cela ne signifie pas uniquement couper électriquement une machine.

L'arrêt peut prendre plusieurs formes :

- suspendre une action ;
- retirer un outil à un agent ;
- révoquer un droit ;
- désactiver un workflow ;
- revenir à une version précédente ;
- passer en mode manuel ;
- isoler un composant ;
- désactiver un modèle ;
- geler une décision en attente de contrôle.

Le droit d'arrêt devient donc un principe d'architecture.

Un système que personne ne peut interrompre dans des conditions prévues n'est pas réellement gouverné.

## Réversibilité

L'arrêt protège l'instant.

La réversibilité protège la trajectoire.

Une organisation doit pouvoir revenir sur une configuration, changer de fournisseur, remplacer un modèle, exporter ses données, reconstruire un service ou restaurer un processus humain lorsque cela est nécessaire.

L'automatisation ne doit pas détruire silencieusement les chemins alternatifs qui permettraient cette réversibilité.

Cela pose un problème concret : une procédure entièrement automatisée pendant plusieurs années peut faire disparaître la compétence humaine permettant de la reprendre manuellement.

Le maintien de la capacité de reprise doit donc être gouverné lui aussi.

## Séparation des pouvoirs numériques

Le livre propose une analogie prudente avec la séparation des pouvoirs.

Un même composant ne devrait pas nécessairement pouvoir :

1. définir la règle ;
2. interpréter la situation ;
3. autoriser l'action ;
4. exécuter l'action ;
5. certifier lui-même que son action était correcte.

Cette concentration peut être efficace.

Elle réduit aussi les possibilités de contradiction et de contrôle.

Dans les usages sensibles, il peut être utile de séparer certaines fonctions entre agents, services ou personnes distinctes.

Cette séparation n'est pas obligatoire partout.

Elle doit être proportionnée au risque.

## Le coût de la gouvernance

La gouvernance n'est pas gratuite.

Chaque contrôle ajoute potentiellement :

- délai ;
- charge cognitive ;
- coût de maintenance ;
- friction d'usage ;
- responsabilité documentaire.

Un système peut donc devenir ingouvernable par excès de contrôle autant que par absence de contrôle.

La question n'est pas de maximiser les validations humaines.

Elle est de placer les contrôles là où leur valeur dépasse leur coût.

Cette logique rejoint la parcimonie attentionnelle introduite dans C08.

## Gouvernance continue

Le NIST AI RMF décrit la gouvernance comme une fonction transversale et continue du cycle de vie.

Cette idée est fondamentale.

Un système ne devient pas gouverné parce qu'un comité a approuvé sa mise en production une fois.

Les modèles changent.

Les données changent.

Les usages dérivent.

Les équipes changent.

Les réglementations évoluent.

Les risques apparaissent parfois après déploiement.

La gouvernance doit donc inclure surveillance, réévaluation, retrait et décommissionnement.

## Vers le SIIAOS

Les quatre chapitres de cette partie permettent maintenant de poser le problème général.

L'IA introduit des sorties probabilistes.

Elle peut devenir une interface avec les connaissances.

Elle peut être intégrée dans des agents capables d'utiliser des outils.

Mais aucune de ces capacités ne définit à elle seule une architecture gouvernable.

Il faut une structure qui relie :

**intelligence, mémoire, action et gouvernance.**

C'est l'objet de la partie suivante consacrée au SIIAOS.

## Hypothèse de travail

> **Une automatisation est gouvernée lorsqu'il est possible d'identifier qui définit ses finalités, qui possède les droits d'action, qui peut la contrôler, qui peut l'interrompre et qui assume les conséquences.**

Cette définition est volontairement opérationnelle.

Elle sera testée dans les chapitres ultérieurs sur les agents, l'immeuble SIIAOS, les droits progressifs et les architectures territoriales.

## Statut des affirmations

**Faits sourcés** : le NIST AI RMF définit la gouvernance comme continue et transversale ; l'AI Act impose un contrôle humain effectif pour les systèmes à haut risque relevant de son article 14.

**Doctrine** : chaîne observer → proposer → décider → autoriser → exécuter → vérifier → rendre compte ; droit d'arrêt ; séparation proportionnée des fonctions numériques.

**À tester** : critères permettant de mesurer l'effectivité d'un contrôle humain, coût optimal des validations et préservation des capacités de reprise manuelle.
