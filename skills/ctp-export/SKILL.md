---
name: ctp-export
description: Compile tous les livrables CTP d'un projet (persona, offre, positionnement, voix, compliance) en un seul fichier vérifiable avec scorecard de complétion, GÉNÈRE un pitch puissant (méthode SIRA, < 3 min) à partir de toutes les données, et maintient un document de référence vivant consulté pour la suite du projet. Use when the user asks "exporter mon travail CTP", "générer le livrable", "compiler mes docs", "export CTP", "préparer pour envoi", "rapport de mon projet", "génère mon pitch", "crée mon pitch", "mon elevator pitch", or wants a single shareable text of all CTP work.
metadata:
  version: 1.2.0
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
| Marque (branding + positionnement + différenciateur) | `positionnement/<slug>.md` |
| Voix | `voix/<slug>.md` |
| Compliance | `ctp/tariqa-compliance.md` |

## Deux entrées

- **Export complet** (« export CTP », « génère le livrable ») → toute la procédure ci-dessous.
- **Pitch seul** (« génère mon pitch », « crée mon pitch », « mon elevator pitch ») → **ne pas
  forcer l'export complet**. Lire ce qui existe déjà (`ctp/REFERENCE-<slug>.md` en priorité, sinon
  les docs présents), générer le pitch via `references/pitch.md` à partir de ce qu'on a, et
  **signaler les briques manquantes** (« pitch partiel : offre pas encore définie → la résolution
  reste floue ; on fait l'offre pour un pitch complet ? »). Sortir le pitch dans un bloc de code.
  Ne pas écrire de fichier d'export, ne pas recalculer tout le scorecard.

## Procédure (export complet)

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
6. **Générer le PITCH (méthode SIRA)** à partir de persona/offre/positionnement/voix —
   suivre `references/pitch.md`. L'inclure dans l'export ET dans le doc de référence.
   Si une brique manque (ex. offre non définie), faire un pitch partiel + le signaler.
7. **Mettre à jour le document de référence vivant** `ctp/REFERENCE-<slug>.md`
   (voir section dédiée) — c'est le doc consolidé à consulter pour toute la suite.
8. Proposer un **export HTML** lisible si demandé (un seul fichier autonome), et un
   **PDF** si le membre veut l'envoyer/imprimer (générer via l'outil PDF, ou « Imprimer
   → Enregistrer en PDF » depuis le HTML).
9. **Inviter à publier dans le Collectif Tariqa PRO** (voir section dédiée).
10. **Garde-fous CTP avant export** : vérifier qu'aucun chiffre d'argent ni mot
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
| 3. Marque | … | … |
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
## 3. Marque (branding + positionnement)
<contenu intégral de positionnement/<slug>.md>

---
## 4. Voix
<contenu intégral de voix/<slug>.md>

---
## ✓ Compliance
<contenu intégral de ctp/tariqa-compliance.md>

---
## ★ Pitch (méthode SIRA)
<pitch court ~30 s> · <pitch complet < 3 min : hook + Situation + Impact + Résolution + Appel à l'action>
<3-5 punchlines marketing réutilisables> — généré selon references/pitch.md, dans la voix du membre.
```

## Bloc copier-coller (pour envoi rapide)

À sortir dans un bloc de code, court :

```
LIVRABLE CTP — <projet> — <date>
Avancement : <X>/4 étapes complètes
Persona ✅ · Offre 🟡 · Marque ⬜ · Voix ⬜ · Compliance ⬜
Points ouverts : <n>
Fichier complet : ctp/EXPORT-<slug>-<date>.md
```

## Le document de référence vivant — `ctp/REFERENCE-<slug>.md`

En plus des exports datés (photos figées), maintenir **un seul** document vivant qui
représente l'**état courant consolidé** du projet : `ctp/REFERENCE-<slug>.md`.

- **Écrasé à chaque export** (≠ les `EXPORT-<slug>-<date>.md` qui s'accumulent comme
  historique). C'est la **source consolidée à jour**.
- **À consulter pour toute la suite du projet.** C'est le mémo central : avant de
  coacher, d'écrire un contenu, de prendre une décision, on relit cette référence pour
  rester cohérent avec la cible, l'offre, le positionnement et la voix déjà définis.
  Les autres skills (parcours, voix, coach-zaki…) doivent le lire en priorité s'il existe.
- Même structure que le gabarit d'export (en-tête + scorecard + contenu intégral), mais
  daté « dernière mise à jour : <AAAA-MM-JJ> ».

## Publier dans le Collectif Tariqa PRO (Circle)

L'export n'a de valeur que s'il est **partagé** : l'animateur (Zaki) le voit, le membre
s'engage devant le collectif, et chacun publie son avancement au fur et à mesure.

- Après l'export, **inviter le membre à le publier dans l'espace dédié** du Collectif
  Tariqa PRO sur Circle. Le lien est centralisé dans `references/collectif.md` (le lire) :
  **SIRAT — LE FAMEUX PARCOURS** → https://collectif-tariqa-pro.circle.so/c/sirat-le-fameux-parcours
- Format au choix du membre : **coller le bloc copier-coller** (résumé + scorecard) ou
  **uploader le PDF** complet.
- Le skill ne poste pas à la place du membre (il n'a pas accès à Circle) : il prépare le
  contenu prêt à coller/joindre et donne le lien de l'espace.
- Tonalité : « Publie ton livrable dans l'espace du Collectif Tariqa PRO — comme ça Zaki
  voit ton travail et tu t'engages devant le groupe. »

## Garde-fous

- **Ne rien inventer** : l'export reflète l'état réel des fichiers. Un doc absent
  est marqué ⬜, pas rempli à la volée.
- Le scorecard doit rendre **visible** le vrai niveau de travail (un projet plein
  de `⏳` n'est pas « complet »).
- Pas de chiffres d'argent dans le bloc copier-coller.
- L'export est une **photo datée** : ne pas écraser un export précédent, en créer
  un nouveau (date dans le nom).
