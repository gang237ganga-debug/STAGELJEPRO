# LJE — environnement PWA / APK

Cette version conserve le prototype LJE HTML/CSS/JavaScript existant et ajoute uniquement l'environnement nécessaire pour le rendre installable comme PWA et le préparer à un empaquetage Android.

## Contenu
- `www/index.html` : prototype LJE existant + manifest/service-worker déclarés.
- `www/manifest.json` : identité, icônes, affichage standalone et URL de démarrage.
- `www/service-worker.js` : cache de l'application et fonctionnement hors-ligne de l'app shell.
- `www/icons/` : icônes Android/PWA 192 et 512 px.
- `netlify.toml` / `vercel.json` : déploiement statique avec en-tête adapté au service worker.
- `package.json` : serveur local de test.

## Important : pour obtenir l'APK avec PWABuilder
PWABuilder travaille à partir d'une **URL HTTPS publique** d'une PWA. Un ZIP local ne suffit pas pour générer l'APK via son interface.

1. Déployer le dossier `www/` sur un hébergement HTTPS (Netlify, Vercel, GitHub Pages, etc.).
2. Ouvrir l'URL publique dans PWABuilder.
3. Laisser PWABuilder analyser le manifest et le service worker.
4. Choisir **Package → Android**.
5. Configurer le nom `LJE`, l'identifiant de package et la signature.
6. Générer le package Android pour test/sideload ou publication.

## Test local
Avec Node.js :

```bash
npm install
npm start
```

Pour tester l'installation PWA sur téléphone, utiliser ensuite une URL HTTPS publique. Le service worker n'est pas conçu pour être considéré comme installé depuis `file://`.

## Limite actuelle
La base de données du prototype reste la BDD JavaScript/localStorage du prototype. Le paiement reste fictif. Aucun backend réel ou paiement réel n'est ajouté ici.
"# STAGELJEPRO" 
