# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'état (_state_) pour contrôler l'affichage d'un composant ✔️ : hook de react permettant de changer l'état d'une variable sur le DOM généralement. Prend 2 paramètres : une constante et une fonction modifiant la constante
- les composants enfants et les _props_ qu'on leur passe ✔️ : les props vont toujours du parent vers l'enfant. Cela permet de récupérer des données dans le composant enfant depuis le composant parent et ainsi éviter de répéter son code (DRY!!)
- le déclenchement d'instructions en fonction des actions de l'utilisateur ✔️ à l'aide de différentes fonctions react comme onClick ou onChange et du state
- le déclenchement d'instructions en fonction de l'étape du cycle de vie du composant ou du changement de valeur de ses props ✔️ : utilisation du hook react useEffect qui soit se rend perpetuellement si pas de tableau de dépendance, se rend qu'une fois avec un tableau de dépendance vide ou se rend à chaque changement d'une variable si celle-ci est mise dans le tableau de dépendance
- l'usage d'un reducer (_useReducer_) pour gérer un état composé dans un composant
- l'état stocké dans un composant avec un _context provider_ et accessible dans ses descendants via `useContext` ✔️ : le context permet de déployer un "context" sur toute l'application à l'aide du context.Provider qui est ensuite appelé en haut de l'application dans le fichier app.js. Très utile pour l'authentification sur une application par exemple 

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```javascript
// tokenContext.jsx
import React, { createContext, useMemo, useState } from 'react';

export const TokenContext = createContext();

function TokenContextProvider({ children }) {
 
    const [token, setToken] = useState("");
    const tokenShare = useMemo(() => ({token, setToken}), [token, setToken]);
 
  return (
    <TokenContext.Provider value={tokenShare}>
      {children}
    </TokenContext.Provider>
  );
}

export default TokenContextProvider;

//App.js
import Footer from "./components/Footer";
import Header from "./components/Header";
import Main from "./components/Main";
import TokenContextProvider from "./context/tokenContext";

const App = () => {
  return (
    <TokenContextProvider>
      <Header />
      <Main />
      <Footer />
    </TokenContextProvider>
  );
};

export default App;

```

### Utilisation dans un projet ✔️

[lien github](https://github.com/JenniferDELEO/Betaseries-clone)

Description : un clone du site betaséries (site de gestion de séries et films) avec l'utilisation de leur API en react (site commencé avant la rentrée et loin d'être fini)

### Utilisation en production si applicable❌ / ✔️

[lien du projet](https://github.com/Plinn/monoceros_mobile)

Description : projet 3 de la formation dev et dev mobile en 5 mois de WCS : suivi des colis en temps réels avec plusieurs paramètres étudiés comme les chocs, la température, l'humidité...

### Utilisation en environement professionnel ❌

Description :

## 🌐 J'utilise des ressources

### Titre

- lien : https://grafikart.fr/formations/react
- description : série de vidéos tuto sur react

- lien : https://stackoverflow.com/
- description : site d'entre-aide de développeurs

- lien : https://fr.reactjs.org/
- description : doc officielle sur react

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
