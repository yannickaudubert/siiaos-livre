---
type: chapitre
id: C02
partie: 1
version: v0.2
status: draft
updated: 2026-08-08
claims_reviewed: partial
source_ids: [SRC-NIST-DIGID-001, SRC-EUDI-001, SRC-W3C-DID-001]
tags: [identite-numerique, federation, pseudonymes, souverainete-relationnelle]
---
# C02 · L'individu poly-identitaire

Une personne n'a pas plusieurs identités au sens humain du terme parce qu'elle possède plusieurs comptes.

Elle possède en revanche plusieurs **représentations numériques**, plusieurs identifiants, plusieurs ensembles d'attributs et plusieurs relations de confiance.

Cette distinction paraît simple. Elle évite pourtant une grande partie de la confusion qui entoure l'identité numérique.

## Identité, identifiant, preuve et authentification

Les travaux techniques contemporains distinguent plusieurs fonctions qui sont souvent mélangées dans le langage courant.

La **preuve d'identité** cherche à établir avec un niveau d'assurance donné qui est une personne dans un contexte déterminé.

L'**authentification** cherche ensuite à vérifier que la personne qui revient est bien le titulaire déjà enrôlé.

La **fédération** permet à un fournisseur d'identité ou de justificatifs de transmettre des assertions à plusieurs services distincts.

Un **identifiant** n'est qu'un moyen de désigner un sujet dans un système.

Un **attribut** décrit une caractéristique : âge, qualification, rôle professionnel, droit d'accès, adresse ou appartenance.

Cette décomposition change la manière de poser le problème.

Nous ne cherchons plus « l'identité numérique unique » d'une personne.

Nous cherchons à comprendre **quels systèmes détiennent quelles représentations, avec quel niveau d'assurance, pour quel usage et sous quelle gouvernance**.

## Une personne, plusieurs contextes

Dans la vie quotidienne, une même personne peut être simultanément :

- citoyen pour une administration ;
- salarié ou prestataire pour une organisation ;
- assuré pour un organisme social ;
- client pour une banque ;
- auteur pour une plateforme ;
- professionnel certifié dans un métier ;
- utilisateur pseudonyme dans une communauté ;
- sujet statistique dans un système d'analyse.

Aucune de ces représentations ne décrit la personne entière.

Elles répondent à des finalités différentes.

Le problème apparaît lorsque les frontières entre contextes deviennent invisibles ou lorsque des attributs produits dans un contexte migrent vers un autre sans que la personne puisse comprendre ou contester cette circulation.

## La poly-identité comme fragmentation des relations

Le terme **individu poly-identitaire** est conservé dans ce livre, mais sa définition est resserrée.

Il ne désigne pas une personne psychologiquement multiple.

Il désigne une personne dont l'existence numérique est répartie entre plusieurs contextes d'identification, d'authentification, de réputation et de décision.

Cette fragmentation possède deux faces.

Elle peut protéger.

Séparer plusieurs contextes évite qu'un acteur connaisse tout d'une personne.

Elle peut aussi fragiliser.

Une erreur, une incohérence ou une décision prise dans un système peut devenir difficile à corriger si les relations entre représentations sont opaques.

Le but n'est donc pas nécessairement de fusionner les identités.

Il est de rendre leurs relations **compréhensibles, minimales et gouvernables**.

## Divulgation sélective plutôt que copie généralisée

Le cadre européen de l'identité numérique et les standards d'identifiants décentralisés montrent une autre manière de penser cette relation.

Un service n'a pas toujours besoin de connaître l'ensemble d'une identité.

Il peut avoir besoin de vérifier uniquement un attribut.

Être majeur.

Posséder une qualification.

Être autorisé à agir au nom d'une organisation.

Le principe de **divulgation sélective** devient alors plus intéressant qu'une logique dans laquelle chaque service copie un dossier complet.

La souveraineté relationnelle commence peut-être ici : pouvoir prouver ce qui est nécessaire sans rendre visible tout ce qui ne l'est pas.

## Pseudonymat et continuité

Le pseudonyme n'est pas l'opposé de l'identité.

Il peut être une identité contextuelle stable.

Dans certains espaces, ce qui importe n'est pas de connaître l'état civil d'une personne, mais de savoir que le même acteur revient, qu'il possède certains droits ou qu'il assume une continuité de comportement.

Le règlement européen sur l'identité numérique reconnaît explicitement la possibilité de générer et conserver des pseudonymes dans le portefeuille européen lorsque l'identification légale n'est pas requise.

Cette possibilité est importante pour le SIIAOS.

Un système distribué n'a pas besoin d'exiger une identité civile globale pour toutes les interactions.

Il doit pouvoir adapter le niveau de preuve à la finalité et au risque.

## De la souveraineté identitaire à la souveraineté relationnelle

Le mot souveraineté peut devenir trompeur s'il laisse penser qu'une personne maîtrise seule l'ensemble des systèmes avec lesquels elle interagit.

Une identité est toujours relationnelle.

Un diplôme implique un émetteur.

Un droit implique une autorité ou une organisation.

Une authentification implique un service qui accepte une preuve.

Une réputation implique des observateurs et des critères.

La question n'est donc pas seulement « qui possède mon identité ? ».

Elle devient :

> **Qui peut établir, demander, transmettre, vérifier, combiner ou révoquer les attributs qui me représentent dans un contexte donné ?**

Cette question prépare le principe central de la suite du livre : **connexion sans fusion**.

## Hypothèse de travail

Nous proposons de définir la souveraineté relationnelle comme :

> **la capacité d'une personne ou d'une organisation à comprendre et gouverner les relations entre ses différentes représentations numériques, sans devoir les fusionner dans une identité universelle.**

Cette définition est doctrinale.

Elle doit encore être testée sur des cas réels : identité administrative, identité professionnelle, délégation, organisations multi-employeurs, pseudonymat, authentification locale et fédération inter-organisations.

## Sources de travail

- `SRC-NIST-DIGID-001` · NIST SP 800-63-4 et volumes associés, 2025.
- `SRC-EUDI-001` · Règlement (UE) 2024/1183 établissant le cadre européen relatif à une identité numérique.
- `SRC-W3C-DID-001` · W3C Decentralized Identifiers (DIDs), v1.0 Recommendation et v1.1 Candidate Recommendation.

## Statut des affirmations

**Faits sourcés** : séparation technique entre preuve d'identité, authentification et fédération ; existence de mécanismes de divulgation sélective, pseudonymes et contrôle utilisateur dans le cadre EUDI ; standards DID visant le contrôle d'identifiants indépendamment d'un registre central unique.

**Observation** : les individus interagissent avec de multiples contextes de représentation numérique.

**Doctrine** : souveraineté relationnelle, connexion sans fusion.

**À tester** : métriques de fragmentation identitaire, coûts de fédération, risques liés aux corrélations entre pseudonymes et limites concrètes du contrôle utilisateur.
