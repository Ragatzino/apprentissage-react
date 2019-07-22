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

## Exercice 0 : Créer votre premier composant
