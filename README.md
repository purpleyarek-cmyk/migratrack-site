# Site de MigraTrack

Site de présentation de l'application iOS MigraTrack. Il contient aussi les pages qu'Apple demande pour publier une app : **Support** et **Politique de confidentialité**.

Le site est entièrement statique (HTML et CSS). Il ne dépose aucun cookie et ne charge aucune ressource externe.

## Pages

| Fichier | Rôle | URL à donner à Apple |
|---|---|---|
| `index.html` | Accueil, présentation de l'app | Marketing URL (facultative) |
| `support.html` | Contact et aide | **Support URL (obligatoire)** |
| `confidentialite.html` | Politique de confidentialité | **Privacy Policy URL (obligatoire)** |
| `mentions-legales.html` | Mentions légales (obligatoires en France) | — |
| `404.html` | Page d'erreur | — |

## Mettre le site en ligne avec GitHub Pages

1. Sur GitHub, ouvrez le dépôt → **Settings** → **Pages**.
2. Dans « Build and deployment », choisissez **Deploy from a branch**, puis la branche `main` et le dossier `/ (root)`. Cliquez sur **Save**.
3. Une à deux minutes plus tard, le site est en ligne à l'adresse `https://purpleyarek-cmyk.github.io/migratrack-site/`.

## À compléter avant de donner les liens à Apple

- [ ] Remplacer `contact@migratrack.example` par la vraie adresse e-mail dans tous les fichiers.
- [ ] Remplir les champs surlignés en jaune dans `mentions-legales.html` et `confidentialite.html` (nom de l'éditeur, statut, adresse, fournisseur de messagerie).
- [ ] Vérifier que la politique de confidentialité décrit exactement ce que fait l'app : stockage uniquement sur l'iPhone, pas de compte, pas de serveur, pas de statistiques. Si l'app utilise iCloud, HealthKit, des notifications ou un outil d'analyse, il faut le dire.
- [ ] Remplacer la maquette d'écran de l'accueil par de vraies captures de l'app, si vous le souhaitez.
- [ ] Une fois l'app publiée, ajouter la bannière App Store (balise commentée dans le `<head>` de `index.html`).

## Référencement Google

1. Ouvrez [Google Search Console](https://search.google.com/search-console) et ajoutez la propriété « Préfixe de l'URL » : `https://purpleyarek-cmyk.github.io/migratrack-site/`.
2. Choisissez la validation par **balise HTML** : copiez la balise `<meta name="google-site-verification" …>` dans le `<head>` de `index.html`, poussez, puis cliquez sur Valider.
3. Dans **Sitemaps**, envoyez `sitemap.xml`.

Note : `robots.txt` n'est lu par les moteurs que lorsque le site est à la racine d'un domaine. Sur l'adresse github.io actuelle, il est ignoré ; le sitemap s'envoie donc par Search Console.

Si l'adresse du site change (nom de domaine), mettez à jour les balises `canonical` et `og:` de chaque page, `sitemap.xml` et `robots.txt`.

## Plus tard : nom de domaine

Pour utiliser un domaine comme `migratrack.fr`, achetez-le chez un registraire (OVH, Gandi…), puis indiquez-le dans **Settings → Pages → Custom domain**. Si vous changez de domaine, remplacez `migratrack-site` dans la balise `<base>` de `404.html`.
