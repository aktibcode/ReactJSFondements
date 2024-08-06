# Chapitre : PROPS REACT PAR DEFAUT


# Accessoires par défaut

Comme nous l'avons dit au début, les props sont une idée fondamentale de l'architecture de React.
Réfléchissons un instant à quelque chose. Si nous avons utilisé un prop dans un composant mais que nous oublions d'envoyer sa valeur depuis le composant parent, cela produira intrinsèquement des problèmes dans l'exécution. Pour cette raison, React fournit une technique qui nous aidera énormément. Cette technique s'appelle les **props par défaut** .

Ce code définit un composant ReactHeader très simple qui restitue un `<h1>`élément contenant un titre pour la documentation d'une version particulière de React.

```
// Simple React Component
function ReactHeader(props) {
 return <h1>React {props.version} Documentation</h1>;
}
```

Dans le composant ReactHeader, nous allons définir la version de la propriété sur 18. Tout le reste semble fonctionner correctement dans le composant ReactHeader.

```
//We are going to render ReactHeader with version=’18’
const  App = () => { return <ReactHeader version=’18’ />}
//output on the screen :          
//React 18 Documentation

```

# Accessoires par défaut

Que se passe-t-il lorsque la propriété version n'est pas transmise ?
Vous l'avez probablement deviné. Voici ce qui se passe lorsque le composant ReactHeader est rendu sans la propriété version :

```
// Simple React Component
function ReactHeader(props) {
 return <h1>React {props.version} Documentation</h1>;
}
```

Étant donné que la propriété version n'est pas transmise, la référence à props.version dans le composant n'est pas définie.
Le résultat à l'écran sera :

```
//output on the screen :  
React undefined Documentation
```

# Solution:

Vous pouvez résoudre ce problème en définissant le `default props`dans le composant :

```
// Simple React Component
function ReactHeader(props) {
 return <h1>React {props.version} Documentation</h1>;
}

// Set default props
ReactHeader.defaultProps = {
 version: "16"
};
```

Le composant va utiliser la **valeur par défaut** pour la propriété de version chaque fois qu'elle n'est pas transmise.

# Accessoires par défaut avec syntaxe de déstructuration

Alternativement, avec la syntaxe de déstructuration d'objet ES6, vous pouvez déstructurer les accessoires d'un composant fonctionnel avec des valeurs par défaut.

```
// Simple React Component
function ReactHeader(props) {
 // default value of version is 18
 const { version = "18" } = props;
 return <h1>React {version} Documentation</h1>;
}
//Or;
// default value of version is 18
function ReactHeader({ version = "18" }) {
 return <h1>React {version} Documentation</h1>;
}
```

Le composant va utiliser la valeur par défaut pour la propriété de version chaque fois qu'elle n'est pas transmise.
