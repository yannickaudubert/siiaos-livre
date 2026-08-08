---
type: chapitre
id: C11
partie: 3
version: v0.2
status: draft
updated: 2026-08-08
claims_reviewed: partial
source_ids: [SRC-REACT-001, SRC-TOOLFORMER-001, SRC-NIST-GENAI-001]
tags: [agents, outils, permissions, orchestration, multi-agents]
---
# C11 · Agents et équipes d'agents

Un modèle de langage qui répond à une question n'est pas nécessairement un agent.

Le terme devient utile lorsqu'un système peut poursuivre un objectif à travers plusieurs étapes, observer des résultats intermédiaires, choisir ou appeler des outils et modifier son comportement en fonction de ce qu'il reçoit.

Une définition de travail peut être formulée ainsi :

> **Un agent est une boucle logicielle orientée objectif qui combine perception d'un contexte, production d'une décision intermédiaire, usage éventuel d'outils, observation du résultat et poursuite conditionnelle de l'action.**

Cette définition ne suppose aucune autonomie politique ou morale.

Elle décrit un mécanisme logiciel.

## Du modèle à la boucle d'action

Les travaux comme ReAct ont montré l'intérêt de combiner raisonnement en langage et actions externes dans une même boucle. Toolformer a également exploré la capacité de modèles à apprendre quand et comment appeler des outils.

Ces travaux marquent un changement d'architecture.

Le modèle ne produit plus seulement du texte destiné à un humain.

Sa sortie peut devenir une instruction destinée à une fonction, une API, un moteur de recherche, un interpréteur, une base de données ou un autre agent.

Cette transition augmente fortement l'importance des permissions.

Une erreur textuelle peut induire un utilisateur en erreur.

Une erreur agentique peut aussi déclencher une action.

## L'agent n'est pas son modèle

Un agent comprend plusieurs éléments :

- un ou plusieurs modèles ;
- une consigne ou politique ;
- un contexte ;
- une mémoire éventuelle ;
- un ensemble d'outils ;
- des droits ;
- une logique d'arrêt ;
- des mécanismes de journalisation ;
- parfois une validation humaine.

Changer le modèle ne change donc pas nécessairement la fonction de l'agent.

Inversement, conserver le même modèle tout en modifiant ses outils ou ses droits peut transformer radicalement son niveau de risque.

Le SIIAOS doit par conséquent inventorier **les capacités effectives**, et pas uniquement les noms des modèles installés.

## Un outil est une extension de capacité

Lorsqu'un agent reçoit un outil, il reçoit un nouveau pouvoir d'action.

Lire un fichier.

Interroger une base.

Écrire un document.

Envoyer un message.

Créer un ticket.

Modifier du code.

Déployer un service.

La liste des outils constitue donc une partie du modèle de sécurité.

Elle doit être observable, versionnée et limitée selon le contexte.

Un agent ne devrait pas recevoir « tous les outils disponibles » par commodité.

Il devrait recevoir le minimum de capacités nécessaire à sa fonction.

## Permissions progressives

Nous pouvons distinguer plusieurs niveaux de capacité agentique :

**Observer** : lire un contexte sans produire d'effet externe.

**Proposer** : produire une recommandation ou un plan.

**Préparer** : générer un artefact sans le publier ni l'exécuter.

**Exécuter en sandbox** : agir dans un environnement isolé et réversible.

**Exécuter sous validation** : préparer une action nécessitant une autorisation humaine ou institutionnelle.

**Exécuter dans un périmètre délégué** : agir automatiquement dans des limites précises.

Cette gradation correspond mieux au risque réel qu'une opposition binaire entre agent « autonome » et agent « non autonome ».

## Plusieurs agents ne forment pas automatiquement une équipe

Ajouter plusieurs agents peut produire davantage de diversité de raisonnements.

Cela peut aussi produire :

- répétitions ;
- conflits ;
- coûts de calcul ;
- dilution des responsabilités ;
- propagation d'erreurs ;
- conversations sans valeur ;
- inflation documentaire.

Une équipe d'agents doit donc avoir une raison d'exister.

Chaque rôle doit apporter une fonction distincte : recherche, critique, vérification, simulation, architecture, contrôle juridique, exécution, etc.

Le désaccord peut être utile.

La duplication inutile ne l'est pas.

## Orchestration et responsabilité

Un orchestrateur peut décider quel agent intervient, dans quel ordre et avec quels outils.

Mais l'orchestrateur lui-même devient alors un composant critique.

Qui définit les règles d'escalade ?

Qui choisit le seuil nécessitant une validation humaine ?

Que se passe-t-il lorsqu'un agent refuse ou échoue ?

Qui possède la priorité lorsque deux recommandations s'opposent ?

L'architecture multi-agents déplace donc le problème de coordination au lieu de le supprimer.

## Mémoire et contamination

La mémoire d'un agent doit être limitée à ce dont il a réellement besoin.

Une mémoire globale partagée entre tous les agents simplifie parfois l'implémentation mais augmente les risques de fuite de contexte, de contamination entre projets et de propagation d'informations obsolètes.

Le principe **connexion sans fusion** s'applique donc aussi aux agents.

Ils peuvent partager une information ou une capacité sans partager l'intégralité de leurs mémoires.

## Agent jetable, rôle durable

Le SIIAOS doit également éviter l'inflation agentique.

Un rôle peut être durable sans que son agent le soit.

Pour une tâche ponctuelle, il peut être préférable d'instancier un agent temporaire, lui fournir un contexte minimal, conserver les traces utiles puis détruire son état.

Cette logique rejoint une architecture frugale : conserver les méthodes et les preuves, pas nécessairement tous les processus vivants.

## Hypothèse de travail

> **La gouvernance d'un agent doit porter d'abord sur ses capacités, ses outils et ses droits, avant de porter sur sa personnalité ou son modèle.**

Cette proposition prépare l'immeuble SIIAOS, dans lequel chaque agent devra être visible par fonction, état, droits et objectifs.

## Statut des affirmations

**Faits sourcés** : les travaux ReAct et Toolformer documentent des architectures reliant modèles de langage et actions ou outils externes.

**Doctrine** : niveaux de capacité agentique, agent jetable / rôle durable, inventaire des capacités effectives, mémoire compartimentée.

**À tester** : métriques utiles pour décider quand plusieurs agents surpassent une architecture plus simple, coût réel de l'orchestration et seuils de permissions selon les métiers.
