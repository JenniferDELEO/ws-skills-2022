# Langage Javascript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les `structures` de base du langage ✔️ : élément script dans un fichier HTML ou fichier à part appelé dans le fichier HTML. Utilisé souvent pour manipuler le DOM
- les normes `ecmascript` ✔️ : le nommage des variables (let et const au lieu de var), les templates string (``), les "arrow-function"...
- l'utilisation de l'`asynchrone` ✔️ : le système des Promises pour obtenir une réponse future à une requête à l'aide de async/await avec try{} catch {} ou .then().catch()
- les spécifités du mot-clef `this` ❌

## 💻 Je code en Javascript

### Un exemple de code commenté ❌ / ✔️

```javascript
const promptFunction = () => {
    let text;
    let date = prompt("Écrivez une année", "2018");
    if (date === null || date === "") {
      text = "Autre";
      setFilterCreationDate(filterCreationDate.filter((a) => a !== date));
    } else {
      text = "Autre : " + date;
    }
    document.getElementById("otherDate").innerHTML = text;
    filterCreationDate.includes(date)
      ? setFilterCreationDate(filterCreationDate.filter((a) => a !== date))
      : setFilterCreationDate((prevState) => {
          return [...prevState, date];
        });
  };
```

### Utilisation dans un projet ✔️

[lien github](https://github.com/JenniferDELEO/Betaseries-clone)

Description : un clone du site betaséries (site de gestion de séries et films) avec l'utilisation de leur API en react (site commencé avant la rentrée et loin d'être fini)

### J'ai utilisé ce langage en production ✔️

[lien du projet](https://github.com/Plinn/monoceros_mobile)

Description : projet 3 de la formation dev et dev mobile en 5 mois de WCS : suivi des colis en temps réels avec plusieurs paramètres étudiés comme les chocs, la température, l'humidité...

### J'ai utilisé ce langage en environement professionnel ❌

Description :

## 🌐 J'utilise des ressources

### Titre : StackOverflow

- lien : https://stackoverflow.com/
- description : site d'entre-aide de développeurs


- lien : https://grafikart.fr/formations/debuter-javascript et https://grafikart.fr/formations/react
- description : série de vidéos tuto sur javascript et sur react

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

