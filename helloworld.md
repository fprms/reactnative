# Modifier le projet de base

* Importer les libraires
* Créer le composant
* Afficher (render) le composant


**React** et **ReactNative** sont deux librairies différentes.
La librairie **React** décrit comment un composant doit se comporter et comment les assembler et les faire travailler ensemble.
La librairie **ReactNative** permet de rendre le composant sur l'écran du périphérique mobile et permet également d'accéder à des composants natifs.

`Import` fait partie d'ES6. Par défaut, les fichiers n'ont pas accès aux variables globales contenues dans d'autres fichiers. Il faut donc les importer.

## Créer un composant

Un composant (React ou ReactNative) est un Object (dans ce cas-ci une fonction) qui produit du contenu à afficher sur l'écran. Pour définir notre objet, nous allons créer une fonction. Cette fonction doit retourner un objet qui décrit ce qui doit apparaître sur l'écran. Cette fonction accepte l'injection de données arbitraires via des propriétés (props).

Pour créer un composant, il faut donc créer une fonction stockée dans une `const` et lui donner le contenu à retourner. La forme de cette fonction est un peu différence de ce que vous avez pu voir jusqu'à présent, il s'agit d'une *arrow function* (anonyme, plus concis, retour implicite (on écrit pas le return), pas de liaison pour this).

```javascript
const myApp = () => {
    return();
};
```

ReactNative propose une série de [composants natifs](https://facebook.github.io/react-native/docs/components-and-apis.html) dont `<Text></Text>` que nous allons utiliser ici. De prime abord, la syntaxte peut vous paraître singulière et c'est normal. Il ne s'agit pas de JavaScript mais d'une extension d'ECMAScript appelée [JSX](https://facebook.github.io/jsx/) et developpée par Facebook. Cette syntaxe comporte une série d'avantages:

* Plus rapide, il est optimisé en Javascript lors de la compilation.
* Les erreurs peuvent être relevée lors de la compilation.
* Sa syntaxe proche du HTML est simple à prendre en main.

```javascript
const myApp = () => {
    return(<Text>Hello World !</Text>);
};
```
## Afficher (enregistrer) le composant

Une fois que le composant est créé, il faut dire à l'application de l'afficher. Il est important de noter que l'enregistrement du composant principal via Expo ne se fait pas de la même manière. Par défaut, Expo nomme votre fichier principal `App.js`. Si vous désirez le renommer, veillez à suivre [cette procédure](https://docs.expo.io/versions/latest/sdk/register-root-component.html).
```javascript
AppRegistry.registerComponent('nom_du_projet'), () => nom_du_composant);
```

## Déstructurer l'`import` et refactorisation du code
Pour la réalisation de ce composant, nous avons mobilisé deux éléménts provenant de la librairie ReactNative. Cependant, nous importons toujours l'entièreté de la librairie. Dans un souci d'optimisation, nous allons déstructurer notre `import` pour ne garder que les éléments dont nous avons besoin. Déstructurer est une technique qui permet d'extraire du contenu d'un `Array` ou `Object` vers une nouvelle variable.

```javascript
import {Text, AppRegistry} from 'react-native';
```

## Modularisation
Un des gros avantages de React et ReactNative est de décomposer une application en une série de composants qui pourront être réassembler selon différentes configurations. Nous allons donc modulariser notre code afin que notre composant ne se trouvent plus directement dans le fichier d'index.

* Créer un nouveau fichier JavaScript : `nom_du_composant.js`
* Importer les librairies et les déstructurer.
* Créer le composant
* Exporter le composant : `export default nom_du_composant`
* Importer `nom_du_composant` `from` `'chemin_relatif_vers_le_fichier_js`
* Insérer le composant à l'endroit voulu
