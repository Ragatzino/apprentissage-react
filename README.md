# Exercice 0 - Configuration et lancement d'un projet

## Un peu de configuration

- Une fois node installé (vous pouvez vérifier la version de node `node -v` et celle de npm `npm -v`), ajoutez la commande globale `npm install --global create-react-app` si ce n'est pas déjà fait.

- Pour créer une application React, il suffit d'exécuter la commande `create-react-app mon-appli`. Pour la lancer on se place dans le dossier `cd mon-appli` puis `npm start`.

- dans vscode installer l'extension eslint (cd mon-appli puis `npm info "eslint-config-airbnb@latest" peerDependencies` && `npx install-peerdeps --dev eslint-config-airbnb` pour la config d'airbnb par exemple) et ajouter un fichier .eslintrc contenant : `{ "extends": "airbnb" }` pour linter comme airbnb.

* dans vscode installer l'extension prettier permettant de formatter votre code, ce qui permet de formatter proprement votre code et donc a terme de clarifier les changements git dans votre projet.

## Architecture projet React

```
Appli
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

Remarque personnelle : Un choix intéressant a été fait sur Nautile, pour plus de clarté du code, on a réuni les composants qui composent un même bloc fonctionnel ensemble : ex formulaire et gestion de formulaire // Tout ce qui attrait au tableau de bord // etc..

Nous appliquerons cette structure dans le prochain exercice.
