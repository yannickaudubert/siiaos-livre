---
type: chapitre
id: C10
partie: 3
version: v0.2
status: draft
updated: 2026-08-08
claims_reviewed: partial
source_ids: [SRC-RAG-001, SRC-W3C-PROV-001, SRC-NIST-GENAI-001]
tags: [rag, connaissance, provenance, sources, traceops]
---
# C10 · L'IA comme interface avec la connaissance

L'intelligence artificielle générative peut devenir une interface extrêmement efficace entre une personne et un corpus documentaire.

Elle peut rechercher, résumer, rapprocher, reformuler et synthétiser.

Cette capacité est utile précisément parce qu'elle réduit le coût d'accès à l'information.

Mais elle crée un risque symétrique : plus la synthèse devient fluide, plus l'utilisateur peut oublier qu'elle est une reconstruction.

## Une réponse n'est pas une source

Une réponse produite par un modèle est un artefact généré.

Même lorsqu'elle est correcte, elle ne remplace pas les documents, données ou observations sur lesquels elle devrait s'appuyer.

La première règle est donc simple :

> **La réponse doit permettre le retour à la source.**

Ce retour ne doit pas être purement décoratif.

Une citation qui pointe vers un document sans permettre d'identifier quel passage soutient quelle affirmation apporte une provenance faible.

L'idéal est de pouvoir reconstruire une chaîne :

**affirmation → extrait ou donnée → document → producteur → contexte → date → transformation.**

Cette chaîne constitue un prolongement direct de TraceOps.

## Le RAG améliore l'accès, pas automatiquement la vérité

Les architectures de génération augmentée par recherche, souvent appelées RAG, combinent un modèle génératif avec une mémoire externe ou un système de récupération documentaire.

Le travail fondateur de Lewis et ses coauteurs montrait déjà l'intérêt de combiner mémoire paramétrique et mémoire non paramétrique, notamment pour améliorer l'accès à des informations plus facilement actualisables et fournir de la provenance.

Mais ajouter un moteur de recherche documentaire ne supprime pas mécaniquement les erreurs.

Plusieurs erreurs restent possibles :

- le bon document n'est pas récupéré ;
- un passage pertinent est mal classé ;
- un document obsolète domine un document récent ;
- la question est mal interprétée ;
- le modèle généralise au-delà des passages fournis ;
- une citation correcte est associée à une affirmation qu'elle ne soutient pas réellement.

Le RAG doit donc être considéré comme une **architecture de mise en contexte**, pas comme une garantie de vérité.

## Provenance de l'information et provenance de la génération

Il est utile de distinguer deux provenances.

La première concerne les connaissances utilisées.

D'où vient cette donnée ?

Qui a produit ce document ?

Quand ?

Avec quelle méthode ?

La seconde concerne le processus de génération.

Quel document a été fourni au modèle ?

Quel passage a été sélectionné ?

Quelle version du modèle a généré le résultat ?

Quelles transformations intermédiaires ont été appliquées ?

Le standard W3C PROV fournit depuis longtemps un modèle générique pour représenter des entités, activités, agents et relations de dérivation. Le SIIAOS n'a donc aucune raison de réinventer entièrement la notion de provenance.

Il doit plutôt s'appuyer sur les standards existants et les spécialiser lorsque les chaînes d'IA le nécessitent.

## Le contexte est une ressource gouvernée

Un modèle peut avoir techniquement accès à un document sans avoir juridiquement ou organisationnellement le droit de l'utiliser dans un contexte donné.

Le système de recherche doit donc respecter les mêmes frontières que le reste du SI.

Un utilisateur ne devrait pas récupérer, par l'intermédiaire d'une IA, des informations qu'il ne pourrait pas consulter directement.

Cette exigence semble évidente.

Elle devient pourtant plus difficile lorsque plusieurs espaces documentaires, agents et outils sont reliés.

Le contrôle d'accès doit donc exister **avant la récupération**, et pas uniquement au moment d'afficher la réponse.

## Mémoire paramétrique et mémoire explicite

Un modèle contient des régularités apprises pendant son entraînement.

Cette mémoire paramétrique est utile, mais difficile à inspecter précisément.

Une mémoire documentaire explicite possède d'autres qualités.

Elle peut être datée.

Versionnée.

Corrigée.

Supprimée.

Sourcée.

Restreinte par droits.

Pour des usages organisationnels, la mémoire explicite doit donc rester la référence pour les connaissances qui doivent être prouvées, mises à jour ou auditées.

Le modèle peut aider à les interpréter.

Il ne doit pas devenir l'archive officielle de l'organisation.

## Réponse, preuve et confiance

Une architecture mature peut produire plusieurs niveaux de réponse.

**Réponse exploratoire** : utile pour comprendre un sujet, mais non validée.

**Réponse sourcée** : les affirmations importantes sont reliées à des documents identifiés.

**Réponse vérifiée** : les sources ont été contrôlées selon une procédure déterminée.

**Décision autorisée** : une personne ou un mécanisme habilité assume la décision issue de ces informations.

Ces niveaux ne doivent pas être confondus.

L'interface devrait rendre leur différence visible.

## Du RAG au système de connaissance

Le RAG est une brique.

Le véritable enjeu est plus large : construire un système où une information peut circuler sans perdre son origine, son niveau de confiance, sa date et ses conditions d'usage.

Nous pouvons résumer cette exigence ainsi :

**retrouver → contextualiser → générer → attribuer → vérifier → décider.**

La génération n'est qu'une étape.

## Hypothèse de travail

> **La qualité d'une interface IA avec la connaissance doit être évaluée autant par la facilité de retour aux sources que par la qualité apparente de sa réponse.**

Cette proposition donnera plus tard des critères concrets pour TraceOps, les Vaults, les moteurs RAG locaux et les gardiens épistémiques.

## Statut des affirmations

**Faits sourcés** : le RAG combine génération et mémoire externe ; W3C PROV fournit un modèle de provenance interopérable ; l'existence d'une citation ne garantit pas automatiquement la qualité de son attribution.

**Doctrine** : niveaux de réponse, distinction provenance de l'information / provenance de la génération, priorité de la mémoire explicite pour les connaissances auditables.

**À tester** : métriques d'attribution, coût de conservation des traces, granularité optimale des citations et effets de la provenance visible sur la confiance des utilisateurs.
