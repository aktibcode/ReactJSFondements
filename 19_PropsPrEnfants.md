# Chapitre : PROPS POUR ENFANTS


# Accessoire pour enfants

Faisons un petit rappel sur le HTML. Un élément HTML est la combinaison d'une balise d'ouverture, d'une balise de contenu et d'une balise de fermeture.
Cette approche est toujours valable avec React. On peut créer un composant et passer ou insérer du contenu entre les balises d'ouverture et de fermeture. C'est ce qu'on appelle les enfants React.

```
const App = () => {
 return (
   <div>
     <Welcome>Sarrah </Welcome>
   </div>
 );
};
```

# Utilisation d'accessoires pour enfants

C'est incroyable, n'est-ce pas ? La valeur passée entre les deux balises peut être utilisée par le composant enfant. Seule la syntaxe a changé.
Pour accéder à cette valeur, on utilise `props.children`. Voici un exemple beaucoup plus détaillé ci-dessous :

```
const App = () => {
 return (
   <div>
     <Welcome>Arya Stark</Welcome>
   </div>
 );
};
```

```
const Welcome = props => {
 // whatever is passed between the tags of the component call can be accessed via this syntax
 return <h1>Welcome {props.children}</h1>;
};
```

![](https://i.imgur.com/hrkTIvN.png)

# Quand l'utiliser ?

La documentation de React indique que vous pouvez l'utiliser `props.children`sur des composants qui représentent des « boîtes génériques » et qui « ne connaissent pas leurs enfants à l'avance ».
En termes plus simples, nous l'utilisons chaque fois que nous voulons uniquement afficher du contenu.

<iframe allowfullscreen="true" frameborder="0" src="https://www.youtube.com/embed/R-6NPhBpC-Q?list=PL-w_yrNy8uTaWNAYCFoyW0C0zPm4S9b3v"></iframe>
