# Chapitre : UTILISATION DES COMPOSANTS


# Utilisation d'un composant

Après avoir créé notre premier composant, il est temps de l'utiliser.

Pour ce faire, nous allons revenir à la modularité JavaScript. Pour pouvoir utiliser un module externe dans notre fichier local, nous devons d'abord l'importer.
Voyons un exemple pour consolider cela.

### MonPremierComposant.js

```
import React from "react";

const MyFirstComponent = () => {
 return <h1> hello from my first component </h1>;
};
export default MyFirstComponent;
```

### Application.js

```
import React from "react";
import MyFirstComponent from "./MyFirstComponent";
const App = () => (
 <>
   <MyFirstComponent />
 </>
);
export default App;
```

### Sortir

![](https://i.imgur.com/p8S91Q8.png)

# Utilisation d'un composant

Attachez vos ceintures ! Il est temps de commencer à créer des choses.

Comme on peut le voir, on retrouve le composant MyFirstComponent à l'intérieur de l'App. Il est donc légitime de se demander si la constante App est un composant ou non. La réponse est : Oui, un composant peut être composé de plusieurs autres composants.

```
const App = () => {
 return (
   <div>
     <Header /> // Header Component
     <Footer />
     // Footer Component
   </div>
 );
};
```

Lorsqu'un composant utilise un autre de cette manière, une relation parent-enfant est formée. Dans l'exemple ci-dessus :

* Le composant App est le parent des composants Header et Footer.
* Les composants En-tête et Pied de page sont les enfants du composant App.

# Utiliser un composant comme racine

Nous avons parlé plus tôt de la méthode **ReactDom.render()** dans le chapitre JSX. En fait, cette méthode existe dans le fichier index.js. Ce fichier est appelé le composant racine.

```
import React from "react";
import ReactDOM from "react-dom";
import App from "./App";
const rootElement = document.getElementById("root");//We call this a “root” DOM node because everything inside it will be managed by React DOM.
ReactDOM.render(<App />,rootElement);
```

Vous pouvez remarquer que les applications créées avec React ont un **seul** nœud racine DOM.
