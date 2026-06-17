---
name: ctp-parcours
description: Porte d'entrée et chef d'orchestre de la méthode Collectif Tariqa PRO. Scanne où en est le projet, affiche la carte du parcours (persona → offre → positionnement → voix, + compliance transverse) avec le statut de chaque étape, et lance la bonne étape suivante dans le bon ordre. Use when the user asks "par où commencer", "lance le parcours CTP", "où j'en suis", "étape suivante", "méthode Tariqa PRO", "start CTP", "guide moi", or doesn't know which CTP skill utiliser.
metadata:
  version: 1.0.0
  category: tariqa-pro
---

# CTP Parcours — le chef d'orchestre

Point d'entrée unique de la méthode Collectif Tariqa PRO. Garantit que chaque
membre avance dans **le bon ordre**, sans sauter d'étape, et sait toujours quoi
faire ensuite.

## L'ordre canonique (ne pas dévier)

| # | Étape | Skill | Fichier produit | Dépend de |
|---|---|---|---|---|
| 1 | **Persona** — à qui | `buyer-persona-architect` | `personas/<slug>.md` | — |
| 2 | **Offre** — quoi | `ctp-offre` | `offres/<slug>.md` | persona |
| 3 | **Positionnement** (+ différenciateur) — pourquoi moi | `ctp-positionnement` | `positionnement/<slug>.md` | persona + offre |
| 4 | **Voix** — comment je le dis | `ctp-voix` | `voix/<slug>.md` | persona + positionnement |
| ✓ | **Compliance** — est-ce cohérent CTP | `ctp-compliant` | `ctp/tariqa-compliance.md` | transverse |

**Compliance** n'est pas une étape de fin : c'est un **checkpoint transverse**.
Le recommander après l'offre, après le positionnement, et sur tout contenu produit.

## Ce que fait ce skill à chaque déclenchement

1. **Scanner le projet** — vérifier la présence ET le remplissage de :
   `personas/*.md`, `offres/*.md`, `positionnement/*.md`, `voix/*.md`,
   `ctp/tariqa-compliance.md`.
   Pour chaque : **absent** / **présent mais incomplet** (contient des `⏳ à
   préciser` ou des sections vides) / **complet**.
2. **Afficher la carte du parcours** avec un statut par étape :
   - ✅ complet · 🟡 commencé (des ⏳ restent) · ⬜ pas commencé.
3. **Recommander la prochaine étape** = la première non complète dans l'ordre
   canonique. Expliquer pourquoi en une ligne (dépendance).
4. **Lancer** le skill correspondant (annoncer : « j'ouvre l'étape X »), ou
   laisser le membre choisir s'il veut faire autre chose — mais **prévenir** s'il
   saute une dépendance (« tu attaques l'offre sans persona — l'offre sera plus
   floue ; on fait le persona d'abord ? »).
5. À la fin d'une étape, reproposer la carte + l'étape suivante.

## Règles d'orchestration

- **Ne jamais sauter une dépendance en silence.** Si le membre veut l'étape 3
  sans l'étape 1, le signaler et proposer de remonter — sans bloquer s'il insiste.
- **Une étape à la fois.** Ne pas lancer deux skills en parallèle.
- **Checkpoint compliance** : après l'offre et après le positionnement, proposer
  un passage `ctp-compliant`. Avant tout export, recommander un dernier audit.
- **Multi-projets** : si plusieurs slugs existent (`personas/a.md`,
  `personas/b.md`), demander sur quel projet on travaille avant de scanner.
- **Fin de parcours** : quand les 4 étapes sont ✅ + compliance passée, proposer
  `ctp-export` pour générer le livrable vérifiable.

## Affichage type (exemple)

```
PARCOURS CTP — projet « benti-couture »
1. Persona ............ 🟡 commencé (3 ⏳ ouverts)
2. Offre .............. ⬜ pas commencé
3. Positionnement ..... ⬜
4. Voix ............... ⬜
✓ Compliance .......... ⬜

→ Prochaine étape : finir le Persona (étape 1). J'ouvre `buyer-persona-architect` ?
```

## Garde-fous

- Le parcours guide, il ne fait pas le travail à la place du membre (les skills
  métier interrogent, lui répond).
- Toujours partir de l'état réel des fichiers, jamais d'une supposition.
- Respecter la voix de chaque skill (ce skill ne rédige pas de contenu, il route).
