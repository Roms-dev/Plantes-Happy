# Plantes Happy – site vitrine

Site statique (HTML, CSS, JavaScript) : aucune installation ni étape de build.
Défilement fluide avec [Lenis](https://github.com/darkroomengineering/lenis) (fichier inclus dans `assets/js`).

## Mettre en ligne : GitHub puis Vercel

1. Créez un dépôt vide sur GitHub (par exemple `plantes-happy`).
2. Dans le dossier du site, exécutez :

```bash
git init
git add .
git commit -m "Site vitrine Plantes Happy"
git branch -M main
git remote add origin https://github.com/VOTRE-COMPTE/plantes-happy.git
git push -u origin main
```

3. Sur [vercel.com](https://vercel.com) : **Add New → Project**, importez le dépôt GitHub.
4. Laissez les réglages par défaut (Framework Preset : *Other*, pas de commande de build, dossier racine `./`), puis **Deploy**.
5. Chaque `git push` sur `main` redéploie le site automatiquement.
6. Domaine personnalisé : *Settings → Domains*, puis ajoutez `plantes-happy.fr`.

## À personnaliser

| Élément | Où |
|---|---|
| Adresse e-mail qui reçoit le formulaire | `js/main.js`, constante `CONTACT_EMAIL` |
| Adresse postale, site web | `index.html`, section `#contact` |
| Textes | `index.html` |
| Couleurs et typographies | `css/style.css`, variables `:root` |

## Structure

```
index.html
css/style.css
js/main.js          scénario de défilement
assets/img/         visuels optimisés (WebP)
assets/fonts/       Playfair Display, Montserrat (hébergées localement)
assets/js/          Lenis
vercel.json         en-têtes et cache
```
