# BabyShow — Site public pour GitHub Pages

**Source : BabyShow 1.7.0**  
**Développement : JHD Solutions**  
**Responsable des informations de contact / bons cadeaux : Gaëlle Herrero (à confirmer juridiquement)**

## Contenu

- `index.html` — présentation publique de BabyShow.
- `confidentialite.html` — politique de confidentialité pour l'application et l'administration.
- `style.css` — charte graphique responsive BabyShow (aucune dépendance externe).
- `assets/` — illustrations extraites du ZIP BabyShow 1.7.0, converties en WebP pour alléger les pages.
- `favicon.svg` — favicon vectorielle.
- `.nojekyll` — indique à GitHub Pages de publier les fichiers statiques tels quels.

Aucun code Firebase, jeton, fichier d'administration ou APK n'est inclus.

## Publication GitHub Pages (compte jhd-solutions)

1. Sur https://github.com/new, sélectionner le propriétaire `jhd-solutions`.
2. Créer le dépôt PUBLIC `jhd-solutions.github.io` (ne pas utiliser `babyshow-download`).
3. Dans **Add file → Upload files**, déposer **le contenu de ce dossier**, et non le ZIP lui-même. Les fichiers HTML doivent se retrouver à la racine du dépôt.
4. Dans **Settings → Pages**, choisir **Deploy from a branch**, puis branche **main** et dossier **/(root)** ; cliquer **Save**.
5. Après publication, visiter :
   - https://jhd-solutions.github.io/
   - https://jhd-solutions.github.io/confidentialite.html
6. Si les liens ne s'ouvrent pas immédiatement, vérifier la page **Actions** de GitHub et le statut de déploiement dans **Settings → Pages**.

**Important :** Ces URL sont les adresses attendues une fois le dépôt créé et Pages activé. Elles ne sont pas actives tant que ces étapes ne sont pas terminées.

## IMPORTANT : exigences de Google OAuth

Le domaine partagé `github.io` ne garantit PAS le passage de Google Auth Platform « Test » à « En production » : Google peut exiger la vérification DNS d'un domaine qui vous appartient, et une vérification de branding, en particulier pour le scope Gmail sensible `gmail.send`.

Pour une validation fiable :

1. Acheter un domaine contrôlé par JHD Solutions (ex. `jhdsolutions.fr`), **ou** obtenir l'accord du propriétaire d'un domaine existant approprié (ex. domaine professionnel de Gaëlle).
2. Connecter un sous-domaine (ex. `babyshow.jhdsolutions.fr`) au dépôt via **Settings → Pages → Custom domain**, puis créer le CNAME DNS demandé.
3. Activer `Enforce HTTPS`.
4. Vérifier la propriété du domaine dans Google Search Console au moyen d'un enregistrement TXT DNS.
5. Dans Google Cloud > Google Auth Platform > Branding, saisir les URL définitives de la page d'accueil et de la confidentialité.
6. Dans Audience, publier l'application si toutes les exigences sont satisfaites ; éventuellement faire vérifier séparément l'utilisation de l'autorisation Gmail.

Il est possible d'utiliser dès maintenant GitHub Pages pour publier le site, tester son apparence et préparer les documents. **Ne pas présenter `jhd-solutions.github.io` comme une solution garantie pour franchir la vérification OAuth.**

Sources officielles :
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://developers.google.com/identity/verification/authentication-policy-compliance
- https://support.google.com/cloud/answer/13464321

## Validation avant publication

- Vérifier le nom officiel et les coordonnées professionnelles de la responsable du traitement.
- Vérifier les durées réelles de conservation et organiser des purges (notamment après 12 mois pour les contacts sans suite), y compris sur les appareils locaux.
- Vérifier que les éventuelles transmissions à un prestataire tiers et la région de stockage Firebase sont correctement décrites.
- Mettre à jour la notice de confidentialité intégrée à l'application Android (`babyshow/src/privacy.js`) afin qu'elle soit cohérente avec la page publique.
- Vérifier les droits d'exploitation des logos et illustrations.
- Éventuellement faire valider la politique par un juriste / DPO.

## Migration vers un domaine personnalisé

Le contenu utilise des liens relatifs : aucune modification HTML n'est nécessaire lors du passage vers un domaine personnalisé qui pointe vers le site racine.
