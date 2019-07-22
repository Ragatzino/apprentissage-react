# Exercice 1 - State et Props

<details><summary>Rappel sur les composants</summary>
<p>

## Rappel : Un composant c'est bien, mais c'est quoi ?

Un Composant peut être une classe ou une fonction qui renvoie du [JSX](https://reactjs.org/docs/introducing-jsx.html) une syntaxe à mi-chemin entre html et javascript.

```javascript
const maVariableJavascript = "Mon premier essai en react";

return <h1>Du JSX ? {maVariableJavascript}!</h1>;
```

Le JSX doit être encadré de parenthèses () s'il s'étend sur plusieurs lignes, on y introduit du code javascript entre accolades {}.

Il y a plusieurs manières de déclarer un composant `<MonComposant />` qu'on utilisera par exemple dans App.js :

```javascript
import React from "react";
import MonComposant from "./MonComposant";

function App() {
  return <MonComposant />;
}
```

- Une classe qui hérite de React.Component :

```javascript
import React from "react"; // Ou bien import React, {Component} from 'react' et utiliser directement extends Component. Il faut quand même importer React pour pouvoir utiliser le JSX !

export default class MonComposant extends React.Component {
  render() {
    return <h1>Mon premier Composant React !</h1>;
  }
}
```

- Une fonction :

```javascript
import React from "react";

function MonComposant() {
  return <h1>Mon premier Composant React !</h1>;
}

// Équivalent à l'écriture en fonction fléchée :
const MonComposant = () => {
  return <h1>Mon premier Composant React !</h1>;
};

// Ne pas oublier l'export !
export default MonComposant;
```

</p>
</details>
Nous allons réaliser ici une application classique, ayant pour la partie front, un Header, un Body et un Footer. 
Cette application aura pour objectif d'afficher les différents utilisateurs de RocketChat de l'innovation. 
### 1 - Structurez votre projet
<details><summary>Rappel sur la structure projet</summary>
<p>

## Appli

```
Appli(avec App.js et index.html pour SPA)
 └──components
    └──monComposant
        ├── __tests__
        │   └── monComposant-test.js
        ├── monComposant.js (avec jsx dedans)
        ├── monComposant.css (ou à l'interieur du js)
        └── package.json( contenu : {
         "main": "monComposant.js"
            })
└──reducers
    └──monComposantContainer
        ├── __tests__
        │   └── monComposantContainer-test.js
        ├── monComposantContainer.js
        └── monComposantContainer.css (idem)
└──utils
     └──constantes etc..
```

</p>
</details>
Créez un Composant ```javascript monComposant ``` que vous appellerez dans votre App.js

(Il pourra par exemple être rendu comme un <div>Hello World</div>)
