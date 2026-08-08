---
type: chapitre
id: C04
partie: 1
version: v0.2
status: draft
updated: 2026-08-08
claims_reviewed: partial
source_ids: [SRC-EU-GDPR-001, SRC-GOODHART-001, SRC-RANKING-FAIR-001]
tags: [donnees, indicateurs, scores, classement, performativite]
---
# C04 · La donnée qui transforme le réel

Une donnée peut décrire une situation.

Mais dès qu'elle entre dans une décision, un classement, un objectif ou une allocation de ressources, elle peut aussi contribuer à transformer la situation qu'elle décrit.

C'est ce phénomène que ce livre appelle **donnée performative**.

Le terme doit être utilisé avec prudence.

Une donnée n'agit pas seule.

Elle agit à travers un système de règles, d'interprétation, d'incitations et de décisions.

## Décrire n'est pas agir

Une température enregistrée par un capteur ne change pas directement la température.

En revanche, si cette mesure déclenche un système de chauffage, la donnée devient une entrée d'action.

Le même mécanisme existe dans les organisations et les sociétés.

Un score de risque peut modifier un contrôle.

Un indicateur de performance peut modifier le comportement d'une équipe.

Un classement peut modifier la visibilité d'une entreprise.

Une recommandation peut modifier la consommation d'un contenu.

Une catégorie administrative peut modifier l'accès à une prestation.

Dans tous ces cas, il faut distinguer la donnée de la chaîne de décision dans laquelle elle prend place.

## Mesure, donnée dérivée, estimation, hypothèse

Le livre adopte une distinction minimale qui doit être conservée dans tous les chapitres :

1. **Mesure** : observation obtenue par un instrument ou une procédure définie.
2. **Donnée dérivée** : valeur calculée à partir d'une ou plusieurs données.
3. **Estimation** : valeur approchée avec une incertitude explicite ou implicite.
4. **Hypothèse** : proposition qui demande encore à être testée.

Une cinquième catégorie est souvent utile :

5. **Score** : valeur synthétique produite pour classer, prioriser ou décider.

Ces catégories peuvent se ressembler dans une interface.

Elles n'ont pourtant pas le même statut épistémique.

Afficher une estimation avec la même apparence qu'une mesure peut produire une confiance injustifiée.

## Le problème des proxys

Une organisation ne peut pas mesurer directement tous ses objectifs.

Elle utilise donc des indicateurs.

Un indicateur est un proxy.

Il représente imparfaitement un phénomène plus complexe.

Cette simplification est indispensable.

Mais elle devient dangereuse lorsque le système commence à optimiser le proxy comme s'il était l'objectif lui-même.

Les travaux regroupés autour de la loi dite de Goodhart décrivent plusieurs situations dans lesquelles une mesure perd de sa valeur lorsqu'elle devient une cible fortement optimisée.

L'enseignement pour le SIIAOS est important :

> **Plus un indicateur influence une décision, plus il faut observer les comportements qu'il provoque et les écarts entre le proxy et la finalité réelle.**

Cette phrase est une règle de gouvernance, pas une équation universelle.

## Le classement produit de la visibilité

Les systèmes de classement constituent un cas particulièrement important.

Ils transforment plusieurs attributs en ordre relatif.

Premier.

Dixième.

Invisible au-delà d'un seuil.

Cette opération semble parfois purement technique.

Elle possède pourtant des effets concrets.

Une position plus élevée peut attirer davantage d'attention, de demandes, de revenus ou de citations.

Le classement peut alors produire une boucle :

**mesure → classement → visibilité → comportement → nouvelles données → nouveau classement**.

Le système ne se contente plus d'observer une population indépendante de lui.

Il participe à son évolution.

## Décisions automatisées et conséquences

Le RGPD reconnaît depuis plusieurs années que certaines décisions fondées exclusivement sur un traitement automatisé peuvent produire des effets juridiques ou affecter significativement une personne.

Cette règle ne signifie pas que tout score ou toute recommandation relève automatiquement de l'article 22.

Elle confirme néanmoins un principe important : la transformation de données en décision peut avoir une portée suffisamment forte pour nécessiter des garanties spécifiques.

Le livre doit donc éviter de parler de la « donnée » comme d'une substance abstraite.

La bonne unité d'analyse est souvent la chaîne :

**source → transformation → indicateur → règle → décision → effet → nouvelle trace**.

## Les boucles de rétroaction

Une donnée performative peut produire plusieurs formes de boucles.

### Boucle d'incitation

Les personnes adaptent leur comportement à l'indicateur qui les évalue.

### Boucle de sélection

Le système choisit certains profils, qui produisent ensuite davantage de données correspondant aux critères déjà utilisés.

### Boucle de visibilité

Ce qui est mieux classé est davantage vu, donc davantage utilisé, donc davantage mesuré.

### Boucle d'exclusion

Ce qui reste sous un seuil obtient moins d'opportunités et produit moins de signaux susceptibles d'améliorer son score.

Ces catégories sont proposées ici comme grille d'analyse. Elles devront être confrontées à des études de cas.

## Une donnée sans contexte devient une autorité fragile

Le danger n'est pas uniquement l'erreur numérique.

Une valeur peut être exacte et néanmoins mal utilisée.

Un taux moyen peut masquer une distribution.

Une donnée récente peut être comparée à une donnée ancienne produite par une autre méthode.

Un score peut être pertinent pour une population et mauvais pour une autre.

Un indicateur peut rester affiché après la disparition du processus qui justifiait son existence.

La gouvernance des données doit donc inclure le **contexte de validité**.

Pour chaque mesure importante, le système devrait pouvoir conserver :

- producteur ;
- date ;
- méthode ;
- unité ;
- population concernée ;
- résolution ;
- incertitude ;
- transformations ;
- finalité ;
- limites connues.

Cette discipline rejoint directement TraceOps.

## De la donnée performative à la donnée gouvernée

Nous pouvons désormais préciser le concept.

> **Une donnée devient performative lorsqu'elle est intégrée à un dispositif qui modifie les comportements, les allocations, les classements ou les décisions, et contribue ainsi à transformer le phénomène qu'elle mesure ou représente.**

La réponse n'est pas d'interdire les indicateurs.

Elle consiste à rendre visibles les boucles qu'ils produisent.

Un système gouvernable doit donc observer non seulement la donnée initiale, mais aussi **les effets créés par l'usage de cette donnée**.

Cette idée sera réutilisée plus tard pour la gouvernance IA, les droits progressifs, les tableaux de bord territoriaux et les simulations organisationnelles.

## Sources de travail

- `SRC-EU-GDPR-001` · Règlement (UE) 2016/679, notamment dispositions relatives au profilage et aux décisions automatisées.
- `SRC-GOODHART-001` · Travaux sur les effets d'optimisation de métriques et variantes de la loi de Goodhart.
- `SRC-RANKING-FAIR-001` · Travaux académiques sur équité et effets des classements automatisés.

## Statut des affirmations

**Faits sourcés** : existence de garanties RGPD concernant certaines décisions automatisées ; littérature démontrant des dégradations possibles de métriques lorsqu'elles deviennent des cibles ; existence de recherches sur l'équité des classements.

**Observation** : indicateurs, scores et classements sont utilisés comme intermédiaires de décision dans de nombreux systèmes.

**Doctrine** : définition de la donnée performative ; grille mesure / dérivée / estimation / hypothèse / score ; quatre types de boucles de rétroaction.

**À approfondir** : performativité en économie et sociologie, causalité des systèmes de recommandation, audits de scores, méthodes de détection de boucles de rétroaction.
