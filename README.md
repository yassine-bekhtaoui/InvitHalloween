# Invitation Halloween

Une seule page statique : `index.html` (les images sont intégrées dans le fichier).
Pas de build, pas de dépendances.

## Mettre en ligne (GitHub + Vercel)

1. Dans ce dossier :
   ```
   git init
   git add .
   git commit -m "Invitation Halloween"
   git branch -M main
   ```
2. Créer le dépôt et pousser :
   - avec GitHub CLI : `gh repo create invitation-halloween --private --source=. --push`
   - ou sur github.com : créer un dépôt vide, puis
     `git remote add origin <url-du-dépôt>` et `git push -u origin main`
3. Sur vercel.com : **Add New… > Project**, importer le dépôt.
   - Framework Preset : **Other**
   - Build Command : laisser vide
   - Output Directory : laisser vide
   - Cliquer sur **Deploy**
4. Le nom du projet donne l'adresse (`nom.vercel.app`). Il se change dans **Settings > General > Project Name**.

## Mettre en ligne (sans GitHub)

```
npm i -g vercel
vercel          # première fois : répondre aux questions
vercel --prod   # publier
```

## Mettre en ligne sur Netlify

- Avec Git : **Add new project > Import an existing project**, choisir le dépôt GitHub.
  Le fichier `netlify.toml` fournit déjà la configuration (aucune commande de build,
  dossier publié : `.`). Cliquer sur **Deploy**.
- Sans Git : glisser le dossier `invitation-halloween` sur https://app.netlify.com/drop
  puis créer un compte pour « réclamer » le site (sinon il est supprimé rapidement).
  Pour mettre à jour : onglet **Deploys** du site, glisser à nouveau le dossier.

## Mettre à jour

Remplacer `index.html` par la nouvelle version, puis :
```
git add . && git commit -m "Mise à jour" && git push
```
Vercel redéploie tout seul. Sans GitHub : `vercel --prod`.

## Notes

- L'adresse ne change pas d'une version à l'autre.
- La page contient `noindex` : elle n'apparaît pas dans les moteurs de recherche.
- Tester avec un autre téléphone, en navigation privée, avant d'envoyer.
- Sur iPhone : Partager > "Sur l'écran d'accueil" pour l'ouvrir en vrai plein écran.
