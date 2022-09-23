# TypeScript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'intéret de TypeScript dans l'IDE ✔️ : permet de typer les variables et les fonctions. Cela va aider à mettre en évidence des erreurs dans le code directement après l'avoir écrit plutôt que lors du démarrage de l'application/serveur
- les types de bases ✔️ : string / number / boolean / [] / object...
- comment et pourquoi étendre une interface ✔️ : par exemple lorsqu'une interface ressemble à une autre mais avec juste une propriété ou plus en plus on peut récupérer les champs/propriétés/méthodes d'une première interface dans une autre
- les classes et les decorators ❌

## 💻 J'utilise

### Un exemple personnel commenté ❌ / ✔️

```typescript
export interface IWilder {
  id: number;
  name: string;
  city: string;
  description: string;
  skills?: object[];
  grades: object[];
}
function App() {
 const [wildersData, setWildersData] = useState<IWilder[]>([]);
  const [openForm, setOpenForm] = useState(false);
  const [date, setDate] = useState(Date.now());

  useEffect(() => {
    const fetchData = async () => {
      const wildersFromApi = await axios.get(
        "http://localhost:5000/api/wilders"
      );
      const newData = wildersFromApi.data.map((data: IWilder) => {
        const result = {
          id: data.id,
          name: data.name,
          city: data.city,
          description: data.description,
          skills: data.grades.map((grade: any) => {
            return { title: grade.skill.name, votes: grade.grade };
          }),
        };
        return result;
      });
      setWildersData(newData);
    };
    fetchData();
  }, [date]);
  return()}
```

### Utilisation dans un projet ❌

[lien github](...)

Description :

### Utilisation en production si applicable❌

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌

Description :

## 🌐 J'utilise des ressources

### Titre

- lien : https://www.typescriptlang.org/
- description : site officiel sur typescript

- lien : https://grafikart.fr/formations/typescript
- description : série de vidéos tuto sur typescript


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
