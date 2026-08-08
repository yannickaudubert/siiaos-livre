---
type: chapitre
id: C05
partie: 2
version: v0.2
status: draft
updated: 2026-08-08
claims_reviewed: partial
source_ids: [SRC-SEI-TD-001, SRC-OECD-DGO-2026-001]
tags: [accumulation, systeme-information, complexite, patrimoine-numerique]
---
# C05 · L'accumulation numérique

Les organisations construisent rarement leur système d'information en une seule fois.

Elles l'accumulent.

Un logiciel répond à un besoin.

Un autre arrive après une réorganisation.

Une nouvelle obligation réglementaire ajoute un contrôle.

Un métier adopte un outil spécialisé.

Un prestataire installe une plateforme.

Une crise impose une solution rapide.

Une équipe crée un tableur pour contourner une limite du logiciel officiel.

Une automatisation est ajoutée entre deux applications qui ne communiquaient pas.

Puis une nouvelle interface vient masquer cette accumulation.

Chaque décision peut être rationnelle au moment où elle est prise.

C'est l'ensemble qui finit par devenir difficile à comprendre.

## L'accumulation n'est pas un accident

Le mot « accumulation » ne doit pas être compris comme une accusation.

Un système vivant conserve les traces de son histoire.

Les organisations changent de direction, de métiers, de réglementation, de partenaires et de technologies. Elles héritent de logiciels anciens, de contrats, de compétences, d'obligations et de données qu'elles ne peuvent pas simplement supprimer.

Le patrimoine numérique est donc nécessairement historique.

La difficulté apparaît lorsque l'organisation ne sait plus distinguer :

- ce qui est encore indispensable ;
- ce qui est seulement historique ;
- ce qui est redondant ;
- ce qui est devenu un contournement ;
- ce qui crée une dépendance ;
- ce qui n'a plus de propriétaire clair ;
- ce qui coûte davantage à maintenir qu'il ne produit de valeur.

L'accumulation devient un problème de gouvernance lorsqu'elle cesse d'être visible.

## L'optimisation locale peut dégrader le système global

Une équipe peut améliorer son fonctionnement en adoptant un nouvel outil.

À son échelle, le gain est réel.

Mais l'organisation peut simultanément créer :

- une nouvelle identité à administrer ;
- une nouvelle copie de données ;
- un nouveau contrat ;
- une nouvelle compétence à maintenir ;
- une nouvelle surface de sécurité ;
- une nouvelle interface à apprendre ;
- une nouvelle rupture dans la chaîne documentaire.

Ce phénomène crée une tension entre **efficacité locale** et **cohérence globale**.

La réponse ne peut pas être d'interdire systématiquement l'innovation locale.

Une centralisation excessive peut elle aussi ralentir l'organisation et éloigner les outils du travail réel.

Le problème devient donc : comment permettre l'expérimentation sans perdre la capacité de cartographier et gouverner ce qu'elle produit ?

## Le patrimoine invisible

Dans beaucoup d'organisations, la cartographie officielle du système d'information ne suffit pas à décrire le système réellement utilisé.

Le travail quotidien peut dépendre de :

- scripts personnels ;
- macros ;
- tableurs ;
- dossiers partagés ;
- carnets de notes ;
- bases locales ;
- comptes SaaS ;
- automatismes créés par un salarié ;
- procédures transmises oralement ;
- exports et imports manuels.

Ces éléments ne sont pas nécessairement des anomalies.

Ils peuvent représenter l'intelligence adaptative de l'organisation.

Ils deviennent fragiles lorsqu'ils sont indispensables mais invisibles.

La première fonction d'une architecture de transformation n'est donc pas de supprimer immédiatement le « shadow IT » ou les bricolages locaux.

Elle est de comprendre **quelle fonction réelle ils remplissent**.

## De l'inventaire d'outils à l'annuaire de capacités

Une simple liste de logiciels décrit mal un système.

Deux outils différents peuvent fournir la même capacité.

Un seul outil peut fournir plusieurs capacités.

Une capacité critique peut même être assurée par une personne plutôt que par un logiciel.

Le SIIAOS propose donc de déplacer progressivement la cartographie :

**outil → fonction → capacité → dépendances → responsable → données → preuves → risque.**

La question devient moins :

> « Quels logiciels possédons-nous ? »

que :

> **« De quelles capacités dépend notre fonctionnement, qui les fournit et que se passe-t-il si elles disparaissent ? »**

Cette approche ouvre une voie plus utile pour arbitrer l'accumulation.

## L'accumulation comme phénomène dynamique

Un inventaire réalisé une fois devient rapidement obsolète.

Le système doit donc être observé dans le temps.

Une capacité peut apparaître.

Une autre peut devenir critique.

Une dépendance peut disparaître.

Un outil peut devenir obsolète sans être techniquement en panne.

Une nouvelle obligation peut transformer un élément secondaire en composant stratégique.

Nous introduisons donc une première exigence : **la cartographie du système doit être vivante**.

Elle doit pouvoir intégrer les changements sans demander chaque fois une reconstruction complète du modèle.

## Hypothèse de travail

> **L'accumulation devient dangereuse moins par le nombre d'outils que par la perte de visibilité sur les capacités, dépendances et responsabilités qu'ils matérialisent.**

Cette hypothèse devra être testée sur plusieurs types d'organisations.

Un grand SI peut être très gouvernable.

Un petit SI peut être opaque.

Le nombre d'applications n'est donc pas une mesure suffisante de complexité.

## Transition

L'accumulation produit une histoire.

Certaines décisions anciennes continuent ensuite à imposer des coûts aux décisions présentes.

C'est là que commence la notion de [[C06_Dette_organisationnelle|dette organisationnelle]].

## Statut des affirmations

**Faits sourcés** : la dette technique peut résulter de choix avantageux à court terme qui augmentent ensuite complexité et coûts ; certaines dettes dépassent le périmètre d'un projet et nécessitent une gouvernance d'entreprise.

**Observations de terrain** : coexistence fréquente d'outils officiels, contournements, automatisations et procédures informelles dans les organisations complexes.

**Doctrine** : cartographier les capacités plutôt que seulement les applications.

**À tester** : métriques de visibilité d'une capacité, dépendances critiques, âge utile des composants et seuils d'accumulation réellement problématiques.
