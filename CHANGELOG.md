# Changelog — plugin Collectif Tariqa PRO

Le membre voit sa version via `lance le parcours CTP` (affichée en tête).
Pour mettre à jour : voir `GUIDE-MEMBRE.md` §10.

## 1.3.0

- **Nouvelle étape 5 — `ctp-page-de-vente`** : l'aboutissement du parcours pour les
  entrepreneurs (hors e-commerce). Transforme tout le travail (persona, offre, marque,
  voix, pitch) en une **landing page v1 mise EN LIGNE**, pointable depuis les réseaux.
  - CTA qualifié (calendrier Calendly/cal.com et/ou formulaire Tally).
  - Vraies images du membre, **anti AI-slop**.
  - **Hold-back** : la page vend le rendez-vous, pas toute l'offre (grain à moudre pour le call).
  - Différenciateur mis en avant, SEO de base, page statique.
  - Déploiement **Vercel** (compte membre requis), URL en ligne.
  - **Filtre e-commerce** : l'étape ne s'adresse pas aux projets e-commerce.
- **`ctp-taste` inclus dans le plugin** : moteur de design anti-slop (copie de taste-skill,
  substance intacte), utilisé par `ctp-page-de-vente`.
- **Output final complet du parcours** = le pitch + les docs `.md` + la landing page v1.

## 1.2.0

- **Étape 3 fusionnée → `ctp-branding-positionnement`** : le branding (identité,
  associations + anti-association, histoire de marque en 3 temps) rejoint le
  positionnement et le différenciateur en un seul parcours.
- **MVB (Minimum Valuable Brand)** : on pose une marque V1 suffisante pour démarrer
  en une session, puis STOP — fini les cycles de réflexion sans fin.
- **Kit visuel de base** : `ctp-branding-positionnement` produit un `brand/design-kit.md`
  (palette hex, typos, règles) — spec réutilisable pour créer ses visuels.
- **`ctp-brandkit` inclus dans le plugin** : génère les planches visuelles + concepts
  logo à partir du kit, sans aucune install séparée (le rendu d'images dépend de la
  capacité du Claude du membre).
- `ctp-positionnement` est renommé `ctp-branding-positionnement` (la donnée reste
  `positionnement/<slug>.md`).

## 1.1.0

- **Coach Zaki** — coach qui challenge au lieu de flatter (modes Actif / Sur demande).
- **Pitch SIRA** dans `ctp-export` + génération **à la demande** (« génère mon pitch »)
  sans passer par l'export complet.
- **`ctp-init`** : au 1er lancement, `ctp-parcours` crée l'arborescence du projet
  (`personas/`, `offres/`…) + injecte le bloc `CLAUDE.md` + ancre la racine
  (`ctp/project.json`).
- **Référence vivante** `ctp/REFERENCE-<slug>.md` maintenue à la fin de **chaque** étape
  (plus seulement à l'export).
- Coach Zaki **propose son mode au 1er contact** s'il est appelé hors parcours.
- Lien de publication Circle réel et centralisé (`references/collectif.md`).
- Doctrine `ctp-compliant` versionnée (signale une version plus récente).
- Métadonnées harmonisées : tous les skills en `category: tariqa-pro`, version unique.
- Correctif : Coach Zaki lisait `offre/` (singulier) au lieu de `offres/`.

## 1.0.0

- Parcours guidé : persona → offre → positionnement → voix.
- Audit de cohérence `ctp-compliant`.
- Export vérifiable `ctp-export` (scorecard + bloc copier-coller).
