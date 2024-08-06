# Chapitre : ACCESSOIRES REACT (REACT PROPS)


# Introduction

Comme la plupart des grandes inventions, il existe toujours une idée de base simple qui maintient tout ensemble. Dans React, c'est sans doute le système **de props** qui nous permet de traiter les composants React comme des fonctions JavaScript.
Nous allons maintenant examiner les props React, notamment :

Quels sont ces accessoires ?

Comment créer un accessoire ?

Les différents types d'accessoires.

Quels sont les accessoires pour enfants ?

Comment définir les accessoires par défaut ?

Quels sont les types d’accessoires ?

# Flux de données unidirectionnel

Vous vous souvenez quand nous avons présenté les fonctionnalités de React ? Nous avons parlé du **flux de données unidirectionnel** . Qu'est-ce que cela signifie, demandez-vous ?

Cette approche signifie que les données ne peuvent circuler, de manière unidirectionnelle, que d'un composant parent vers un composant enfant (de haut en bas) et non l'inverse. Contrairement à d'autres bibliothèques et frameworks, React s'assure que cette fonctionnalité reste dans son architecture.

La raison pour laquelle React conserve cet avantage dans son écosystème est que le flux de données unidirectionnel facilite le traçage des données et de leurs modifications dans l'arborescence des composants. Cela semble un peu déroutant, mais regardons une illustration pour clarifier davantage le concept.

![](https://i.imgur.com/H7TBduU.png)

# Que sont les accessoires ?

Pour rendre possible ce flux de données unidirectionnel, React utilise **des props** .
Les props ou **propriétés** sont les outils que React utilise pour transmettre des données des éléments parents aux éléments enfants.
Considérons-les comme un paramètre dans une fonction JavaScript.
Nous pouvons modifier la valeur de ce paramètre mais les ensembles d'instructions à exécuter restent les mêmes.
Prenez votre page Facebook par exemple. Vous trouverez votre nom à droite, à côté de votre photo.
D'un point de vue de codage, les développeurs Facebook ne peuvent pas créer une barre de navigation personnalisée pour chaque profil.
Cela n'est possible et réalisable qu'en utilisant les props de React.
La structure de ces éléments sera fixée et le contenu (nom, url de l'image...) sera reçu comme un props.

![](https://i.imgur.com/kb3Kk0h.png)

# Exemple JS

Voici un autre exemple pour consolider ce dont nous venons de parler.

```
function Greeting(name) {
return "hello " + name;
}
console.log(Greeting('Jon Snow'))// it will display "hello Jon Snow"
console.log(Greeting('Ramsay Bolton')) // it will display "hello Ramzay Bolton"
console.log(Greeting('I am nobody')) // it will display "hello I am nobody"
```

La fonction Greeting reçoit un nom comme argument. Cependant, quel que soit le nom que nous définissons, elle affichera toujours un concaténé `hello`à côté du nom.

# Exemple de réaction

Essayons maintenant la même idée avec un composant React.

```
function Greeter(props) {
 return <h1>hello {props.name}</h1>;
}
// And invoking the <Greeter/> component…
const App = () => {
 return (
   <div>
     <Greeter name="world" /> {/* 💥 "world" is the prop value*/}
     <Greeter name="I am the King" /> {/* 💥 "I am the King" is the prop value*/}
   </div>
 );
};
export default App;
```

### Sortir

![](https://i.imgur.com/Yod50fb.png)

# Résumons!

Les props React sont comme des arguments de fonction en JavaScript et des attributs en HTML. Pour envoyer des props dans un composant, utilisez la même syntaxe que les attributs HTML :
`<Greeter name="world" />`

```
function Greeter(props) {
 return <h1>hello {props.name}</h1>;
}
```

Comme nous pouvons le voir, le composant Greeter reçoit le nom en tant que props et l'affiche dans une balise h1. Une autre chose à garder à l'esprit est que les props sont un objet et que tout ce que nous passons en tant qu'attributs dans le composant est appelé dans le parent.
Remarque : les props sont immuables, ce qui signifie que l'enfant ne peut lire que le contenu d'un props. Il ne peut pas le modifier.
