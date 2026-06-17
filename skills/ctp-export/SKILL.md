---
name: ctp-export
description: Compile tous les livrables CTP d'un projet (persona, offre, positionnement, voix, compliance) en un seul fichier texte vérifiable, avec un scorecard de complétion (ce qui est rempli vs à préciser), pour que le membre puisse l'envoyer et que l'animateur vérifie le travail. Use when the user asks "exporter mon travail CTP", "générer le livrable", "compiler mes docs", "export CTP", "préparer pour envoi", "rapport de mon projet", or wants a single shareable text of all CTP work.
metadata:
  version: 1.0.0
  category: tariqa-pro
---

# CTP Export — livrable unique vérifiable

Compile les documents de référence CTP d'un projet en **un seul texte** que le
membre peut envoyer (WhatsApp, email, Drive) et que l'animateur peut **vérifier**
d'un coup d'œil : qui a vraiment fait le travail, et où ça reste à compléter.

## Sources compilées (dans l'ordre du parcours)

| Étape | Fichier |
|---|---|
| Persona | `personas/<slug>.md` |
| Offre | `offres/<slug>.md` |
| Positionnement (+ différenciateur) | `positionnement/<slug>.md` |
| Voix | `voix/<slug>.md` |
| Compliance | `ctp/tariqa-compliance.md` |

## Procédure

1. **Identifier le projet** : si plusieurs slugs, demander lequel exporter.
2. **Récupérer la date du jour** (`date +%F`) et lister les fichiers présents.
3. **Calculer le scorecard de complétion** pour chaque doc :
   - **absent** ⬜ · **commencé** 🟡 (contient des `⏳`/sections vides) ·
     **complet** ✅.
   - compter les marqueurs `⏳ à préciser` / champs `<…>` non remplis.
4. **Assembler le fichier** `ctp/EXPORT-<slug>-<AAAA-MM-JJ>.md` selon le gabarit
   ci-dessous : en-tête + scorecard + liste des points ⏳ ouverts + contenu intégral
   de chaque doc.
5. **Produire aussi un bloc copier-coller court** (résumé + scorecard) à coller
   directement dans un message — dans un bloc de code.
6. Proposer un **export HTML** lisible si demandé (un seul fichier autonome).
7. **Garde-fous CTP avant export** : vérifier qu'aucun chiffre d'argent ni mot
   interdit ne traîne dans les docs ; si oui, le signaler (ne pas bloquer l'export,
   mais avertir). Recommander un dernier `ctp-compliant` si pas fait.

## Gabarit du fichier d'export

```markdown
# Livrable CTP — <Nom du projet>
> Membre : <nom> · Date : <AAAA-MM-JJ> · Généré par skill `ctp-export`

## Scorecard de complétion
| Étape | Statut | Points ouverts |
|---|---|---|
| 1. Persona | ✅ / 🟡 / ⬜ | <n ⏳> |
| 2. Offre | … | … |
| 3. Positionnement | … | … |
| 4. Voix | … | … |
| ✓ Compliance | … | dernier verdict : <✅/⚠️/❌ + date> |

**Avancement global : <X>/4 étapes complètes.**

## Points encore à préciser (⏳)
- [Persona] <…>
- [Offre] <…>
- …

---
## 1. Persona
<contenu intégral de personas/<slug>.md>

---
## 2. Offre
<contenu intégral de offres/<slug>.md>

---
## 3. Positionnement
<contenu intégral de positionnement/<slug>.md>

---
## 4. Voix
<contenu intégral de voix/<slug>.md>

---
## ✓ Compliance
<contenu intégral de ctp/tariqa-compliance.md>
```

## Bloc copier-coller (pour envoi rapide)

À sortir dans un bloc de code, court :

```
LIVRABLE CTP — <projet> — <date>
Avancement : <X>/4 étapes complètes
Persona ✅ · Offre 🟡 · Positionnement ⬜ · Voix ⬜ · Compliance ⬜
Points ouverts : <n>
Fichier complet : ctp/EXPORT-<slug>-<date>.md
```

## Garde-fous

- **Ne rien inventer** : l'export reflète l'état réel des fichiers. Un doc absent
  est marqué ⬜, pas rempli à la volée.
- Le scorecard doit rendre **visible** le vrai niveau de travail (un projet plein
  de `⏳` n'est pas « complet »).
- Pas de chiffres d'argent dans le bloc copier-coller.
- L'export est une **photo datée** : ne pas écraser un export précédent, en créer
  un nouveau (date dans le nom).
