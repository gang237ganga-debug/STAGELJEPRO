# LJE — Prototype unifié

Tous les fichiers nécessaires au prototype sont volontairement placés dans CE SEUL DOSSIER, sans sous-dossier `www` ni `icons`.

## Fichiers
- index.html : application LJE
- manifest.json : configuration PWA
- service-worker.js : cache/offline de l'application
- icon-192.png / icon-512.png : icônes PWA
- vercel.json / netlify.toml : déploiement web
- package.json : serveur local et vérification

## Lancement local
```bash
npm install
npm start
```

Puis ouvrir l'URL affichée par le serveur.

## Important
Les chemins du manifest et du service worker ont été adaptés à cette organisation plate. Les fonctionnalités existantes du prototype ne sont pas séparées ni supprimées.
