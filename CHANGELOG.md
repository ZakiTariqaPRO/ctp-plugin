# Changelog — plugin Collectif Tariqa PRO

Le membre voit sa version via `lance le parcours CTP` (affichée en tête).
Pour mettre à jour : voir `GUIDE-MEMBRE.md` §10.

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
