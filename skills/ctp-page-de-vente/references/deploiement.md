# Déploiement — mettre la page EN LIGNE (Vercel)

But : une **URL publique** (ex. `nom-du-membre.vercel.app`) que le membre pointe depuis
ses réseaux. La page est statique (`landing/`), donc le déploiement est simple.

⚠️ **Prérequis membre** : un **compte Vercel** (gratuit, vercel.com). C'est l'équivalent
de l'abonnement / du compte GitHub : le plugin ne peut pas le fournir. Le dire dès le départ.

## Chemin recommandé — Vercel CLI (Claude pilote si dispo)

1. Vérifier la CLI : `vercel --version`. Absente → l'installer : `npm i -g vercel`
   (nécessite Node ; sinon guider via l'install Node, ou passer au chemin B).
2. Connexion : `vercel login` (le membre confirme par email/navigateur — action manuelle).
3. Déployer depuis le dossier `landing/` : `vercel deploy --prod`.
   - Au 1er run, Vercel pose 2-3 questions (nom du projet, dossier). Répondre simplement.
4. Récupérer l'**URL de production** affichée en fin de commande. C'est elle qu'on donne au membre.

> Si un skill `vercel` est présent dans l'environnement, on peut s'appuyer dessus — mais ne
> jamais le supposer installé. Le chemin CLI ci-dessus suffit.

## Chemin B — sans CLI / non-tech (interface web Vercel)

1. Le membre crée un compte sur vercel.com (connexion Google/GitHub possible).
2. « Add New… → Project ». Pour une page statique simple, le plus direct : déposer le
   dossier `landing/` via un dépôt GitHub, ou utiliser l'import de projet.
3. Vercel déploie et donne l'URL `*.vercel.app`.

## Chemin C — secours rapide (Netlify Drop)

Si Vercel bloque : `app.netlify.com/drop` permet de **glisser-déposer** le dossier `landing/`
et d'obtenir une URL immédiate. Compte requis pour la conserver. Pratique en dépannage.

## Après la mise en ligne

- Donner l'**URL** au membre, vérifier qu'elle s'ouvre (et sur **mobile**).
- L'inviter à la mettre dans ses bios réseaux (Instagram, TikTok, LinkedIn, WhatsApp).
- Mises à jour : ré-éditer `landing/` puis re-déployer (`vercel deploy --prod`) — l'URL reste la même.
- Nom de domaine perso (ex. `prenom.com`) = étape ultérieure facultative, pas pour la v1.

## Garde-fous

- Ne pas committer de secrets dans `landing/` (c'est public).
- Compresser les images avant déploiement (page rapide).
- MVB : une URL `*.vercel.app` propre suffit pour la v1. On ne bloque pas sur le domaine custom.
