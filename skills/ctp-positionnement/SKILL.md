---
name: ctp-positionnement
description: Construit, puis enrichit, le positionnement d'un projet selon l'approche Collectif Tariqa PRO — y compris le module différenciateur (« quel est mon différenciateur ? »). Interroge le membre une question à la fois (catégorie, cible, alternatives, différenciateur prouvé, énoncé de positionnement, messages-clés, anti-positionnement) et écrit un document de référence par projet. Use when the user asks "définir mon positionnement", "mon différenciateur", "qu'est-ce qui me rend unique", "what's my positioning", "me démarquer de la concurrence", "trouver mon angle", or wants to add/validate new info about an existing positioning.
metadata:
  version: 1.1.0
  category: tariqa-pro
---

# CTP Positionnement — architecte de positionnement & différenciateur

Moteur d'interview + document vivant. Pose des questions, **produit un document
de positionnement** (incluant le différenciateur prouvé), puis l'enrichit et le
valide. Méthode : `references/methode.md`. Livrable : `references/gabarit.md`.

Le **différenciateur n'est pas un skill à part** : c'est le cœur de ce skill
(étape 4). « Quel est mon différenciateur ? » se traite ici.

## Principe fondateur — moteur ≠ donnée

- **Le skill** = le moteur. Partageable tel quel.
- **Le positionnement** = la donnée, vit dans le projet sous
  `positionnement/<slug>.md`. Jamais dans le skill.

## Dépendances — le positionnement découle de la cible et de l'offre

Avant de commencer, charger ce qui existe :
- **Persona** (`personas/<slug>.md`) → ce que la cible veut vraiment.
- **Offre** (`offres/<slug>.md`) → ce que tu proposes et ta valeur.
Annoncer ce qu'on a chargé. Si l'un manque, le signaler (« le positionnement
sera plus net avec un persona/une offre ») et capter l'essentiel en express,
sans bloquer.

## Routage : choisir le mode au déclenchement

1. Regarder si `positionnement/` existe et contient des fichiers.
2. **Aucun** → mode **CREATE**.
3. **Présent** :
   - Info / apprentissage nouveau → mode **ENRICH**.
   - Nouveau positionnement distinct (autre marché/offre) → CREATE (nouveau slug).
   - Doute → demander.

Toujours annoncer le mode choisi en une ligne avant de commencer.

## Mode CREATE — interview qui produit le positionnement

1. Lire `references/methode.md`, `references/cadres.md` et `references/gabarit.md`.
   Charger persona + offre si présents.
2. Demander nom court + slug.
3. **Une question à la fois.** Reformuler. Vague → 5 Whys. « Je sais pas » →
   *à préciser*, avancer (ne pas fabriquer).
   Suivre les étapes de `methode.md`, en appliquant les frameworks de `cadres.md` :
   recadrage → cadre de référence (alternatives, parité/différence) → **levier
   dominant (les 6 formes)** → axes stratégiques (Porter, carte, Kotler) →
   discipline de valeur (Treacy) →
   archétype (Mark-Pearson/Aaker) → **différenciateurs (boîte à outils + test du
   concurrent + preuve)** → énoncé de positionnement (Moore) → création de
   catégorie (Blue Ocean/Play Bigger, optionnel) → ancrage CTP.
4. Fin de chaque étape : récap + validation.
5. Écrire `positionnement/<slug>.md` selon `gabarit.md`. Chaque fait : **source** + **date**.
6. Proposer le pointeur de persistance + proposer un audit `ctp-compliant`.

## Mode ENRICH — ajouter sans casser

1. Charger le fichier ciblé en entier.
2. Chaque info passe par **VALIDATE**.
3. Écrire après accord. Section + date + source. Montrer le diff.

## Mode VALIDATE — règle de cohérence (toujours avant écriture)

- **Nouvelle** → proposer où l'ajouter.
- **Confirmation** → noter corroborée.
- **Contradiction** → **ne pas écraser en silence** : montrer les deux, demander,
  archiver l'ancienne en note datée.
- **Hors-cible** → signaler, ne pas ajouter.

## Garde-fous spécifiques au différenciateur

- **Test du concurrent obligatoire** : si un concurrent pourrait dire la même
  phrase, ce **n'est pas** un différenciateur → recommencer.
- Un différenciateur **non prouvé** est une hypothèse, étiquetée comme telle.
  Exiger une preuve (vécu, méthode, résultat observable, parcours).
- Ne pas confondre **parité** (ce que tout le monde offre, table stakes) et
  **différenciateur** (ce que toi seul peux revendiquer crédiblement).

## Cohérence Tariqa PRO

- Le positionnement vise à proposer une **alternative** crédible, utile,
  éthique — pas à écraser. (Doctrine : « proposer une alternative, pas subir ».)
- Anti-positionnement assumé (ce que tu n'es PAS) = un atout, pas un risque.
- Pas de garantie de résultat dans la promesse de positionnement.
- À la fin, proposer de lancer `ctp-compliant` sur le positionnement.
- La **voix** (formulation) = skill voix séparé. Ici on fixe le **fond** (l'angle).

## Persistance

Ligne à ajouter au `CLAUDE.md` du projet :

```
## Positionnement de référence
Positionnement et différenciateur dans `positionnement/<slug>.md` — boussole de
tout contenu, page et message de ce projet (skill `ctp-positionnement`).
```

En CREATE, après écriture, proposer d'ajouter cette ligne.

## Garde-fous

- Une question à la fois. Jamais écrire sans validation.
- Positionnement flou → forcer : 1 catégorie claire + 1 cible précise + 1
  différenciateur qui passe le test du concurrent + 1 preuve.
- Fait validé vs hypothèse : toujours distingués.
- Pas de chiffres d'argent mis en avant dans les sorties publiques.
