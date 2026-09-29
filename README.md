# Ta Galerie

Petite application Vue.js 3 qui affiche une galerie d'images à partir de leurs URL.

## Fonctionnalités

- Ajouter une image en collant son URL puis en cliquant sur « Ajouter »
- Les URL vides ne sont pas ajoutées
- Affichage du nombre total d'images

## Notions Vue utilisées

- `ref` pour les données réactives (l'URL tapée et la liste des images)
- `v-model` pour relier le champ de saisie à la variable `newUrl`
- `@click` pour lancer la fonction `ajouterImage` au clic
- `v-for` pour afficher chaque image de la liste

## Lancer le projet

```sh
npm install
npm run dev
```

Puis ouvrir http://localhost:5173 dans le navigateur.
