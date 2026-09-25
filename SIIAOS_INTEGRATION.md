# Intégration au puzzle SIIAOS

```yaml
siiaos_puzzle_version: "2026-09-25"
integration_status: "SURFACE"
truth_status: "CODED"
authority: "none by default"
canonical_reference: "yannickaudubert/twinSIIAOS/docs/SIIAOS_PUZZLE.md"
```

## Rôle dans le SIIAOS

Corpus éditorial et livre de travail. Il documente, explique et transmet des concepts SIIAOS mais ne constitue pas le runtime ni le canon opérationnel du système.

## Ce que cette brique implique

- Le manuscrit peut expliquer une architecture sans prouver son déploiement.
- Les concepts historiques doivent conserver leur période de validité.
- La publication ne doit pas transformer une proposition en fait observé.

## Ce qui peut l'impliquer

- documentation/publication
- university/learning
- public communication

## Capabilities fournies

- editorial corpus
- conceptual explanations
- versioned manuscript
- public references

## Capabilities consommées

- validated concepts
- sources
- decisions suitable for publication
- epistemic status

## Interfaces et contrats

Les interfaces propres au dépôt restent valides dans leur périmètre, mais elles doivent pouvoir se rattacher aux objets SIIAOS pertinents : Identity, Authority, Mandate, Policy, NeedSpec, ContextPack, Capability, Mission, Decision, OperationRecord, Evidence, DesiredState, ObservedState et ChangeSet.

Aucune interface locale ne doit créer silencieusement une seconde source de vérité.

## Données, autorité et confidentialité

- Les accès sont explicitement bornés par identité, rôle, autorité, mandat et policy.
- `Identity != Role != Authority`.
- Les données client, personnelles, confidentielles ou secrètes restent dans leur périmètre d'autorité.
- Source originale, index, RAG, synthèse, interface et canon sont distincts.
- Une capacité technique ne crée jamais une permission.

## Evidence attendue

- Git history
- source references
- version metadata

Une capacité ne doit être déclarée opérationnelle qu'après preuve adaptée au risque.

## Non-rôles

- runtime
- control plane
- source unique de vérité opérationnelle
- preuve de conformité ou de sécurité

## Truth gates

Toujours distinguer :

`PROPOSÉ != CODÉ != TESTÉ != DÉPLOYÉ != OBSERVÉ != PROUVÉ`

et :

`DesiredState != ObservedState`

Les états runtime doivent être reliés à une preuve datée.

## Conditions de promotion

Une intégration peut progresser de CANDIDATE/CONVERGENCE vers ACTIVE lorsque ses contrats, permissions, données autorisées, tests, preuves, mécanismes de repli et conditions de retrait sont explicites et vérifiés.

## Retrait / rollback

La brique doit pouvoir être remplacée ou retirée sans perdre les sources, décisions, Evidence, provenance et capacité de reprise.

## Référence canonique

Le puzzle complet et le contrat documentaire commun vivent dans `twinSIIAOS/docs/`. Cette fiche locale explique uniquement la place de ce dépôt et ne remplace pas le document canonique.
