---
type: doctrine
status: active
version: v0.2
updated: 2026-08-08
tags: [preuve, provenance, epistemologie, traceops]
---
# Protocole de preuve

## Principe

Le livre distingue explicitement quatre statuts :

1. **Fait sourcé** : affirmation appuyée par une source identifiable et vérifiable.
2. **Observation** : constat issu de l'expérience, d'un terrain ou d'un corpus, sans prétention automatique à l'universalité.
3. **Hypothèse** : proposition explicative ou prédictive à confronter aux faits.
4. **Doctrine / modèle** : construction normative ou architecturale proposée par l'auteur.

## Exigence de provenance

Toute affirmation sensible doit pouvoir répondre à cinq questions :

- Quelle est la source ?
- Quelle est sa date ?
- Quelle est sa nature ?
- Quelle transformation a été appliquée ?
- Quel niveau de confiance lui est attribué ?

## Registre minimal d'une affirmation

```yaml
claim_id: CLM-0001
status: fait_source | observation | hypothese | doctrine
source_ids: []
confidence: faible | moyen | fort
verified_at:
contradictions: []
notes:
```

## Hiérarchie de recherche

Priorité aux textes normatifs, publications scientifiques, standards, documentation primaire et jeux de données des producteurs. Les sources secondaires servent à contextualiser ou à identifier une piste, jamais à effacer la source primaire lorsqu'elle existe.

## Principe adversarial

Une affirmation structurante doit être testée par au moins une question contradictoire :

- Qu'est-ce qui pourrait la rendre fausse ?
- Dans quel contexte cesse-t-elle d'être valable ?
- Quel coût ou risque masque-t-elle ?
- Quelle alternative explique mieux le phénomène ?

## Règle pour l'IA

Une sortie d'IA n'est jamais une source primaire. Elle peut produire une hypothèse, une synthèse, un classement ou une piste de recherche. Le passage vers un fait exige une vérification indépendante.

## Compatibilité TraceOps

Ce protocole donne au livre la même exigence que le système qu'il décrit : revenir du résultat à la trace, de la trace à la provenance, puis de la provenance au contexte de décision.
