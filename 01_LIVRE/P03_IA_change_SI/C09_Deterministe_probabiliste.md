---
type: chapitre
id: C09
partie: 3
version: v0.2
status: draft
updated: 2026-08-08
claims_reviewed: partial
source_ids: [SRC-NIST-GENAI-001, SRC-NIST-AIRMF-001]
tags: [ia-generative, probabiliste, observabilite, evaluation]
---
# C09 · Du déterministe au probabiliste

Un logiciel classique peut être complexe sans être probabiliste.

Lorsqu'une règle est codée explicitement, une même entrée placée dans le même état produit normalement la même sortie. Les erreurs existent, mais elles sont souvent recherchées dans le code, les données, l'environnement ou l'état du système.

Les modèles génératifs introduisent une autre difficulté.

Ils apprennent des distributions à partir de données, produisent des sorties à partir de représentations internes et peuvent générer plusieurs formulations plausibles pour une même demande. Le comportement dépend du modèle, de son contexte, de ses paramètres de génération, des données fournies et des outils éventuellement accessibles.

Cela ne signifie pas que le système serait simplement « aléatoire ».

Cela signifie qu'une partie du comportement ne peut pas être réduite à une suite de règles métier écrites une par une par le concepteur.

## Le test change de nature

Dans un logiciel déterministe, un test peut souvent vérifier qu'une sortie précise est obtenue pour une entrée donnée.

Avec un système génératif, cette logique reste utile pour certaines fonctions, mais elle ne suffit plus.

Il faut aussi évaluer des propriétés.

Exactitude factuelle.

Respect d'un format.

Robustesse à différentes formulations.

Taux de refus correct.

Capacité à citer une provenance.

Sensibilité à une donnée erronée.

Respect des droits d'accès.

Comportement en situation ambiguë.

Le test devient donc partiellement statistique, contextuel et adversarial.

## Une erreur plausible est plus difficile à voir

Une erreur classique peut faire planter un programme.

Une erreur générative peut être grammaticalement parfaite.

C'est une différence importante.

La fluidité linguistique ne constitue pas un mécanisme de vérification.

Le NIST traite notamment la « confabulation » comme un risque propre aux systèmes génératifs : un système peut produire avec assurance un contenu incorrect ou non soutenu par ses données.

Le problème n'est donc pas uniquement la fréquence de l'erreur.

Il est aussi sa détectabilité.

## L'observabilité devient épistémique

Dans une application classique, l'observabilité porte généralement sur des événements techniques : temps de réponse, erreurs, ressources, traces d'exécution.

Ces informations restent nécessaires.

Mais un système intégrant un modèle génératif nécessite une couche supplémentaire.

Quelle information a été fournie au modèle ?

Quelle version du modèle ?

Quels documents ont été récupérés ?

Quels outils ont été appelés ?

Quel résultat intermédiaire a conduit à l'action suivante ?

Quel élément a été présenté comme fait alors qu'il s'agissait d'une inférence ?

Nous appelons ici cette extension **observabilité épistémique**.

Le terme est doctrinal.

Il désigne la capacité à reconstruire non seulement ce que le système a fait, mais également **sur quoi il s'est appuyé pour produire une affirmation ou une décision**.

## L'incertitude n'est pas toujours disponible

Un modèle peut produire une probabilité interne sur le prochain token sans fournir pour autant une mesure fiable de confiance dans la vérité de sa réponse complète.

Une formulation comme « je suis sûr à 90 % » ne doit donc pas être interprétée automatiquement comme une probabilité calibrée.

Lorsque le système doit communiquer de l'incertitude, celle-ci devrait autant que possible provenir d'une méthode explicite : comparaison de sources, évaluation, ensemble de modèles, test statistique ou autre procédure documentée.

## Architecture hybride

Le passage au probabiliste ne signifie pas qu'il faut rendre tout le système probabiliste.

Au contraire.

Les architectures robustes peuvent séparer :

- les composants déterministes pour les règles, validations, calculs et droits ;
- les composants probabilistes pour l'interprétation, la recherche, la classification ou la génération ;
- les contrôles humains lorsque l'enjeu ou l'ambiguïté l'exige.

Cette séparation prépare un principe majeur du SIIAOS : **le modèle d'IA n'est pas le système**.

Il est une capacité insérée dans un système plus vaste qui doit rester gouvernable.

## Hypothèse de travail

> **Plus une sortie générative peut produire d'effets dans le monde réel, plus la chaîne qui relie contexte, modèle, outils, décision et action doit être observable et contrôlée.**

Cette proposition structurera les chapitres suivants.

## Statut des affirmations

**Faits sourcés** : les cadres du NIST pour l'IA générative traitent la confabulation, l'évaluation, la gouvernance et le suivi du cycle de vie comme des enjeux de risque.

**Doctrine** : observabilité épistémique ; séparation explicite des couches déterministes, probabilistes et humaines.

**À tester** : métriques d'observabilité épistémique, seuils de délégation selon le risque et méthodes de calibration pertinentes selon les cas d'usage.
