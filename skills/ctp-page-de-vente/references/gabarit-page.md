# Gabarit — structure de la landing page v1

Page **statique unique** (`landing/index.html` + `landing/style.css` + `landing/images/`).
Direction visuelle via `ctp-taste`. Couleurs/typos depuis `brand/design-kit.md`. Chaque
bloc tire son contenu d'un doc du parcours — ne rien inventer.

## Ordre des sections (de haut en bas)

1. **Hero** — au-dessus de la ligne de flottaison
   - Titre = la promesse (la « une seule chose » + bénéfice principal). Court, clair.
   - Sous-titre = pour qui + ce que ça change (1-2 lignes).
   - **CTA principal** (bouton) → calendrier ou formulaire.
   - 1 **vraie image** (portrait du membre ou visuel de marque). Pas d'image AI.
   - Source : positionnement (énoncé Moore) + persona.

2. **Pour qui / le problème**
   - Nommer la cible et sa douleur réelle, dans SES mots (persona).
   - Le visiteur doit se dire « c'est moi ». 3-4 points max.

3. **La solution / ton offre (sans tout déballer)**
   - Ce que tu proposes et la transformation visée — **pas** le détail complet, les prix,
     ni les modalités. **Hold-back** : on garde le grain à moudre pour le call.
   - Bénéfices avant caractéristiques.

4. **Ton différenciateur** ⭐ (section qui doit sauter aux yeux)
   - Pourquoi toi et pas une autre option. Repris du doc marque (différenciateur prouvé).
   - Court, affirmé, visuellement mis en avant.

5. **Preuve / à propos**
   - Histoire de marque (catalyseur + preuve), qui tu es, pourquoi on peut te faire confiance.
   - **Débutant sans témoignages** : s'appuyer sur l'histoire fondateur, l'engagement, la
     méthode, d'éventuels premiers résultats — **jamais de faux témoignages**. Si rien,
     omettre la preuve sociale proprement (ne pas inventer).

6. **CTA final**
   - Reprend le CTA principal (même destination). Phrase d'action claire.
   - Calendrier (rendez-vous) ou formulaire (voir `cta.md`).

7. **Footer**
   - Mentions simples + « Collectif Tariqa PRO » discret. Lien réseaux si le membre veut.

## Règles de design (via ctp-taste)

- **Anti-slop** : appliquer le pre-flight de `ctp-taste`. Pas de templates génériques, pas
  de dégradés AI tape-à-l'œil, pas d'emojis-déco partout.
- **Couleurs/typos** : strictement celles de `brand/design-kit.md`.
- **Lisibilité** : corps ~16-18 px mini, titres hiérarchisés, beaucoup d'air, 1 idée/section.
- **Mobile d'abord** : la majorité du trafic réseaux vient du mobile. Tester l'affichage étroit.
- **Rapide** : 1 CSS, images compressées, pas de librairie lourde.

## Images — ce qu'on demande au membre

- **Portrait** (lui/elle) — humanise, crée la confiance.
- **Logo** s'il existe (sinon, wordmark simple aux couleurs du design-kit).
- **Visuels de réalisations / contexte** (photos réelles de son travail, lieu, produit).
- À défaut : **aplats de couleur** du design-kit + typographie soignée. Jamais de fausse photo.

## SEO de base (intégrer au HTML)

- `<title>` clair (marque + promesse) + `<meta name="description">`.
- Balises **Open Graph** (og:title, og:description, og:image) pour un bel aperçu en partage.
- HTML **sémantique** (`<header> <main> <section> <footer>`, un seul `<h1>`).
- `lang="fr"`, viewport mobile, favicon si dispo.
