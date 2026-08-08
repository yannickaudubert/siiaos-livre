---
type: registre_sources
version: v0.2
status: active
updated: 2026-08-08
tags: [sources, verification, recherche]
---
# Registre des sources · v0.2

Ce registre n'est pas une bibliographie finale. Il suit les sources déjà vérifiées et leur rôle dans le manuscrit.

## SRC-EU-AIACT-001

- Producteur : Union européenne / EUR-Lex
- Nature : règlement
- Référence : règlement (UE) 2024/1689
- URL : https://eur-lex.europa.eu/eli/reg/2024/1689
- Usage : gouvernance IA, responsabilités, calendrier réglementaire
- Statut : primaire
- Vigilance : calendrier d'application à versionner, certaines échéances ayant été modifiées en 2026.

## SRC-EU-AIACT-2026-001

- Producteur : Union européenne / EUR-Lex
- Nature : règlement modificatif 2026
- Référence : règlement (UE) 2026/1744
- URL : https://eur-lex.europa.eu/legal-content/FR/TXT/?uri=OJ:L_202601744
- Usage : mise à jour des échéances relatives à certaines obligations sur les systèmes à haut risque
- Statut : primaire

## SRC-NIST-AIRMF-001

- Producteur : NIST
- Nature : cadre de gestion des risques
- Titre : Artificial Intelligence Risk Management Framework 1.0
- URL : https://www.nist.gov/itl/ai-risk-management-framework
- Usage : gouvernance continue, cartographie, mesure et gestion du risque IA
- Statut : primaire institutionnel
- Vigilance : AI RMF 1.0 est en cours de révision en 2026.

## SRC-NIST-GENAI-001

- Producteur : NIST
- Nature : profil du cadre AI RMF
- Titre : Artificial Intelligence Risk Management Framework: Generative Artificial Intelligence Profile
- URL : https://www.nist.gov/publications/artificial-intelligence-risk-management-framework-generative-artificial-intelligence
- Usage : risques propres aux IA génératives, provenance, validation, gouvernance
- Statut : primaire institutionnel

## SRC-FAIR-001

- Producteur : GO FAIR / principes issus du corpus FAIR
- Nature : principes de gestion et réutilisation des données
- URL : https://www.go-fair.org/fair-principles/
- Usage : provenance, métadonnées, réutilisabilité, partie TraceOps
- Vigilance : FAIR ne garantit pas à lui seul la qualité scientifique d'une donnée.

## SRC-LOCALFIRST-001

- Producteur : communauté Local-First Software / corpus Ink & Switch
- Nature : principes d'architecture logicielle
- URL : https://localfirstweb.dev/
- Usage : définition technique du local-first
- Vigilance : distinguer la définition logicielle historique de l'extension SIIAOS vers autonomie, souveraineté et gouvernance.

## SRC-NIST-DIGID-001

- Producteur : NIST
- Nature : standard / recommandations techniques
- Référence : SP 800-63-4, Digital Identity Guidelines, révision 4, 2025
- URL : https://pages.nist.gov/800-63-4/
- Usage : C02, distinction preuve d'identité / authentification / fédération, niveaux d'assurance
- Statut : primaire institutionnel

## SRC-EUDI-001

- Producteur : Union européenne / EUR-Lex
- Nature : règlement
- Référence : règlement (UE) 2024/1183 établissant le cadre européen relatif à une identité numérique
- URL : https://eur-lex.europa.eu/eli/reg/2024/1183/oj
- Usage : C02, portefeuille d'identité, divulgation sélective, pseudonymes, contrôle utilisateur
- Statut : primaire

## SRC-W3C-DID-001

- Producteur : W3C
- Nature : recommandation / standard en évolution
- Référence : Decentralized Identifiers (DIDs) v1.0 Recommendation ; v1.1 Candidate Recommendation Snapshot du 5 mars 2026
- URL : https://www.w3.org/TR/did-core/
- Usage : C02, identifiants contrôlables sans dépendance obligatoire à un registre ou fournisseur central unique
- Statut : primaire technique
- Vigilance : distinguer DID v1.0 stable de DID v1.1 encore en Candidate Recommendation en 2026.

## SRC-EU-DMA-001

- Producteur : Union européenne / EUR-Lex
- Nature : règlement
- Référence : règlement (UE) 2022/1925 sur les marchés numériques
- URL : https://eur-lex.europa.eu/eli/reg/2022/1925
- Usage : C03, contrôleurs d'accès, services de plateforme essentiels, contestabilité
- Statut : primaire

## SRC-EU-DSA-001

- Producteur : Union européenne / EUR-Lex
- Nature : règlement
- Référence : règlement (UE) 2022/2065 sur les services numériques
- URL : https://eur-lex.europa.eu/eli/reg/2022/2065
- Usage : C03, risques systémiques, systèmes de recommandation, transparence et atténuation
- Statut : primaire

## SRC-EU-GDPR-001

- Producteur : Union européenne / EUR-Lex
- Nature : règlement
- Référence : règlement (UE) 2016/679
- URL : https://eur-lex.europa.eu/eli/reg/2016/679
- Usage : C04, profilage et certaines décisions fondées exclusivement sur un traitement automatisé
- Statut : primaire

## SRC-GOODHART-001

- Producteurs : littérature académique sur Goodhart et optimisation des proxys
- Nature : articles scientifiques / travaux formels et empiriques
- Références de travail : Manheim & Garrabrant (2018), Fire & Guestrin (2018), El-Mhamdi & Hoang (2024)
- Usage : C04, dégradation possible d'un indicateur lorsqu'il devient une cible fortement optimisée
- Statut : secondaire scientifique / à compléter par versions publiées et DOI lorsque disponibles
- Vigilance : ne pas transformer la formule populaire de Goodhart en loi universelle.

## SRC-RANKING-FAIR-001

- Producteurs : Ke Yang, Julia Stoyanovich
- Nature : article scientifique
- Titre : Measuring Fairness in Ranked Outputs
- URL : https://arxiv.org/abs/1610.08559
- Usage : C04, effets et évaluation de classements automatisés
- Statut : scientifique

## Règle

Toute nouvelle source structurante reçoit un identifiant stable. Les chapitres peuvent référencer cet identifiant dans leur frontmatter ou dans une section `Sources de travail`.
