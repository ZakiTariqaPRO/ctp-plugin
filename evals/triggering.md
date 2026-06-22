# Évals de déclenchement — plugin Collectif Tariqa PRO

But : vérifier que chaque skill se déclenche **quand il faut** et **pas hors contexte**.
Méthode (cf skill `skill-creator`) : faire jouer chaque requête à froid, noter le skill
réellement déclenché, comparer à l'attendu. Cible : 100 % sur should-trigger, 0 faux
positif sur should-not. Itérer les `description` en cas d'écart. Zones sensibles :
`buyer-persona-architect` (persona) et `ctp-voix` (copywriting) — beaucoup de skills
concurrents sur la machine d'un membre.

## ctp-parcours
- ✅ « par où je commence avec le Collectif Tariqa PRO ? »
- ✅ « lance le parcours CTP »
- ✅ « où j'en suis dans ma méthode Tariqa PRO ? »
- ❌ « lance les tests » (rien à voir)
- ❌ « par où commencer pour apprendre Python ? » (hors CTP)

## buyer-persona-architect
- ✅ « je veux construire le persona de mon offre CTP »
- ✅ « définir ma cible pour le parcours »
- ❌ « génère un avatar d'image de profil » (pas un persona marketing)
- ❌ « crée un personnage pour mon roman » (persona ≠ fiction)

## ctp-offre
- ✅ « aide-moi à construire mon offre »
- ✅ « structurer mes formules starter / premium »
- ❌ « fais-moi une offre d'emploi » (autre sens d'« offre »)

## ctp-branding-positionnement
- ✅ « c'est quoi mon différenciateur ? »
- ✅ « comment me démarquer de la concurrence »
- ✅ « définir ma marque » / « mon branding » / « à quoi je veux qu'on m'associe »
- ✅ « mon histoire de marque »
- ❌ « positionne cet élément en CSS » (positionnement technique)
- ❌ « crée-moi un logo » (génération visuelle pure → ctp-brandkit, pas la stratégie de marque)

## ctp-brandkit
- ✅ « génère mes planches de marque »
- ✅ « crée-moi des concepts de logo »
- ✅ « fais-moi une identité visuelle / un univers visuel »
- ❌ « c'est quoi mon différenciateur ? » (stratégie de marque → ctp-branding-positionnement)
- ❌ « édite cette photo » (retouche, pas identité de marque)

## ctp-voix
- ✅ « trouve ma voix de marque »
- ✅ « réécris ce texte pour le rendre plus clair »
- ❌ « transcris cette note vocale » (voix ≠ audio)
- ❌ « change la voix de l'assistant vocal » (TTS)

## ctp-compliant
- ✅ « est-ce que mon offre est Tariqa PRO compliant ? »
- ✅ « audite la cohérence de mon projet avec les valeurs »
- ❌ « est-ce conforme au RGPD ? » (autre conformité)

## ctp-export
- ✅ « export CTP » / « génère le livrable »
- ✅ « génère mon pitch » (entrée pitch-seul, sans export complet)
- ❌ « exporte ce tableau en CSV » (autre export)

## coach-zaki
- ✅ « coache-moi », « sois honnête avec moi », « je tourne en rond depuis des mois »
- ✅ « j'ai pas le temps de m'y mettre » (excuse → challenge)
- ❌ « explique-moi ce bug » (demande technique, pas du coaching)
