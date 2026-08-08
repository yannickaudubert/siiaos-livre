---
type: chapitre
id: C07
partie: 2
version: v0.2
status: draft
updated: 2026-08-08
claims_reviewed: partial
source_ids: [SRC-OECD-DGO-2026-001]
tags: [fragmentation, interoperabilite, donnees, silos, gouvernance]
---
# C07 · La fragmentation

Une organisation peut posséder beaucoup d'informations et rester incapable de produire une vision cohérente.

Le problème n'est alors pas l'absence de données.

Il est leur séparation.

Documents dans une GED.

Décisions dans des courriels.

Données dans des applications métier.

Procédures dans un intranet.

Savoir-faire dans la mémoire des personnes.

Indicateurs dans des tableaux de bord.

Projets dans des outils collaboratifs.

Contrats chez des prestataires.

Chacun de ces espaces peut être utile.

La fragmentation apparaît lorsque les relations entre eux deviennent difficiles à reconstruire.

## Le silo n'est pas toujours un défaut

Le mot « silo » est souvent utilisé comme synonyme de mauvais système.

Cette lecture est trop simple.

Certaines séparations sont nécessaires.

Un service RH n'a pas les mêmes droits qu'un service communication.

Une équipe de recherche peut avoir besoin d'un espace protégé.

Une donnée médicale, financière ou disciplinaire ne doit pas circuler sans contrôle.

La séparation protège parfois la confidentialité, l'autonomie, la responsabilité et la sécurité.

Le problème n'est donc pas l'existence de frontières.

Le problème est l'absence de **passages gouvernés** entre ces frontières.

Cette distinction rejoint le principe développé plus tôt : **connexion sans fusion**.

## Fragmentation des données

Deux systèmes peuvent décrire le même objet avec des modèles différents.

Un client peut devenir usager ailleurs.

Une adresse peut être texte libre dans une application et référentiel structuré dans une autre.

Un projet peut porter plusieurs identifiants.

Une personne peut apparaître sous plusieurs rôles.

L'interopérabilité ne consiste donc pas seulement à connecter deux API.

Elle exige aussi de savoir ce que les données signifient.

Le problème devient sémantique.

Deux champs portant le même nom peuvent désigner des réalités différentes.

Deux champs différents peuvent désigner la même réalité.

Une architecture d'interopérabilité doit donc conserver les correspondances, leurs versions et leurs limites.

## Fragmentation des responsabilités

La fragmentation peut être institutionnelle.

Un processus traverse plusieurs services mais aucun acteur ne possède une vision complète de sa performance ou de ses risques.

Chaque équipe optimise son segment.

La responsabilité globale devient diffuse.

Cette situation est particulièrement visible dans les systèmes publics, les grandes organisations et les chaînes de sous-traitance.

L'OCDE souligne encore en 2026 que les infrastructures numériques ne produisent leur valeur que lorsque les systèmes peuvent réellement échanger et fonctionner ensemble entre organismes et niveaux de gouvernement. Le rapport constate des écarts persistants entre stratégies, infrastructures disponibles et mise en œuvre opérationnelle.

La fragmentation n'est donc pas seulement un héritage informatique.

Elle peut être une propriété de la gouvernance elle-même.

## Fragmentation documentaire

Une décision importante peut être impossible à reconstruire parce que ses éléments sont dispersés.

Le besoin est dans un compte rendu.

L'arbitrage dans un mail.

Le budget dans un tableur.

La justification juridique dans une note.

Le résultat dans un ticket.

La conséquence dans un incident six mois plus tard.

Chaque trace existe.

Mais le récit de la décision a disparu.

C'est ici que TraceOps prendra tout son sens.

L'enjeu n'est pas de mettre tous les documents dans un même dossier.

Il est de conserver les **liens de provenance** entre les traces.

## Fragmentation temporelle

La fragmentation existe aussi dans le temps.

Un système est compris par ses concepteurs au moment de sa création.

Quelques années plus tard, les personnes ont changé.

Les contrats ont changé.

Les usages ont dérivé.

Les raisons initiales ne sont plus visibles.

Une documentation correcte à un instant donné ne suffit donc pas.

Elle doit pouvoir accompagner les transformations du système.

Le problème devient celui de la continuité documentaire.

## Interopérabilité : plus qu'un protocole

L'OCDE définit l'interopérabilité comme la capacité des systèmes à se connecter et échanger des informations entre organisations, niveaux de gouvernement et frontières.

Pour le SIIAOS, nous étendons cette définition opérationnelle à quatre dimensions :

1. **technique** : les systèmes savent échanger ;
2. **sémantique** : les données échangées conservent un sens compréhensible ;
3. **organisationnelle** : les responsabilités et processus permettent réellement l'échange ;
4. **gouvernance** : les droits, finalités et preuves de l'échange sont connus.

Une connexion technique sans les trois autres dimensions produit parfois davantage de confusion.

## Le graphe comme outil, pas comme solution magique

Un graphe documentaire ou de connaissances peut aider à représenter les relations.

Il ne résout pas automatiquement la fragmentation.

Un graphe mal gouverné peut simplement centraliser les erreurs et multiplier les liens sans valeur.

Le modèle devra donc distinguer :

- relation observée ;
- relation déclarée ;
- relation déduite ;
- relation hypothétique ;
- relation périmée.

Cette typologie permettra plus tard au moteur cognitique de naviguer dans le système sans présenter toutes les relations comme également certaines.

## Hypothèse de travail

> **La fragmentation n'est pas l'existence de plusieurs espaces. Elle est l'impossibilité de reconstruire de manière gouvernée les relations nécessaires entre ces espaces.**

Cette définition nous permet de préserver les frontières tout en travaillant sur l'interopérabilité.

## Transition

Chaque fragmentation impose un travail supplémentaire à quelqu'un.

Retrouver.

Comparer.

Vérifier.

Changer d'interface.

Comprendre le contexte.

Ce coût se transforme progressivement en [[C08_Surcharge_cognitive|charge cognitive]].

## Statut des affirmations

**Faits sourcés** : l'OCDE constate encore en 2026 des écarts d'interopérabilité, d'adoption et de mise en œuvre malgré la présence de nombreuses infrastructures numériques publiques.

**Doctrine** : quatre dimensions d'interopérabilité ; fragmentation comme perte de reconstructibilité gouvernée des relations.

**Observations de terrain** : dispersion des décisions, référentiels et responsabilités entre outils et équipes.

**À approfondir** : standards d'interopérabilité sémantique, ontologies, graphes de connaissances, gouvernance des métadonnées et architectures fédérées.
