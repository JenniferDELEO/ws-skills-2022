# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- Comment développer en utilisant un système de *livereloading* (`nodemon` par exemple) ✔️ : installation du package nodemon avec npm i nodemon --save-dev puis modification du script "start" dans le fichier package.json avec "nodemon index.js" par exemple
- La connexion de mon application à une base de données avec et sans ORM/ODM (avec `mongodb` puis `mongoose` par exemple) ✔️ avec mongoose : récupération du package pour connection à la base de données avec mongoose.connect("url", {paramètres}).
- Le développement d'une API REST et GraphQL (avec les packages `express` et `graphql` par exemple) ✔️ : avec express : récupération du package puis création d'une constante "app" pour utiliser la fonction express() puis transformer les données en json avec express.json(). Enfin, création de différentes routes pour réaliser le CRUD.
- *Bonus : la manipulation des fichiers système avec `fs` et l'utilisation des streams en NodeJS* ❌

## 💻 J'utilise

### Un exemple personnel commenté ❌ / ✔️

```javascript
const express = require("express");
const mongoose = require("mongoose");

const stuffRoutes = require("./routes/stuff");
const userRoutes = require("./routes/user");

const app = express();
mongoose
  .connect(
    "mongodb+srv://user:password@cluster0.djgos3o.mongodb.net/?retryWrites=true&w=majority",
    { useNewUrlParser: true, useUnifiedTopology: true }
  )
  .then(() => console.log("Connexion à MongoDB réussie !"))
  .catch(() => console.log("Connexion à MongoDB échouée !"));

app.use(express.json());

app.use((req, res, next) => {
  res.setHeader("Access-Control-Allow-Origin", "*");
  res.setHeader(
    "Access-Control-Allow-Headers",
    "Origin, X-Requested-With, Content, Accept, Content-Type, Authorization"
  );
  res.setHeader(
    "Access-Control-Allow-Methods",
    "GET, POST, PUT, DELETE, PATCH, OPTIONS"
  );
  next();
});

app.use("/api/stuff", stuffRoutes);
app.use("/api/auth", userRoutes);

module.exports = app;

```

### Utilisation dans un projet ❌ / ✔️

[lien github](https://github.com/ComicScrip/lyon-react-mars22-p2g1-api)

Description : création de ce repo dans le cadre du projet 2 de la formation dev et dev mobile en 5 mois de la WCS. Contient les routes pour créer, modifier, supprimer et lire des données sur des livres et sur des localisations de boites à livres

### Utilisation en production si applicable ❌

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌

Description :

## 🌐 J'utilise des ressources

### Titre

- lien : https://grafikart.fr/formations/nodejs
- description : série de vidéos tuto sur nodejs

- lien : https://nodejs.org/en/
- description : doc officielle sur nodejs

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description:

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌
- J'ai fait une [présentation](...) ❌
