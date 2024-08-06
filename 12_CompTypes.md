# Chapitre : COMPOSANTS - TYPES


# Types de composants

Comme nous l'avons dit précédemment, il existe deux types de composants React, cette division s'est produite avant l'apparition de la version 16.8 de React.
Mais pour les besoins de l'apprentissage, il est préférable que nous les connaissions.

Les deux types de composants React sont :

* **Composants de classe :** faisant référence aux classes JavaScript.
* **Composants fonctionnels :** faisant référence à la fonction JavaScript.

# Composants de classe

Si vous lisez des articles sur Internet sur les composants React, vous trouverez les noms suivants qui font référence aux **composants de classe** :

**Smart Component**
React 16.8, la logique n'était implémentée que dans ce type de composant, en raison de l'avantage que les classes offrent sur les fonctions.

**Stateful Component**
février 2019, seule la classe pouvait contenir et gérer l'état JavaScript.

**Container Components**
On l'appelle ainsi parce qu'il contient généralement d'autres nombreux composants (principalement fonctionnels).

Assez de théorie, regardons un exemple :

```
class Greeting extends React.Component {
 render(){
   return <h1>Hi, I’m a smart component!</h1>;
 }
}
```

# Composants fonctionnels :

Ces composants sont purement de présentation et sont simplement représentés par une fonction. Cette fonction prend éventuellement des props et renvoie un élément React à restituer sur la page.

En général, il est préférable d'utiliser des composants fonctionnels dans la mesure du possible en raison de leur prévisibilité et de leur concision. Comme ils sont purement de présentation, leur résultat est toujours le même si nous leur donnons les mêmes accessoires.

Vous trouverez peut-être dans d'autres ouvrages des composants fonctionnels qualifiés d'état, de muets ou de présentationnels. Tous ces noms découlent de la nature simple des composants fonctionnels.

* Fonctionnels car ce sont essentiellement des fonctions
* Apatrides parce qu’ils ne détiennent pas et/ou ne gèrent pas d’État
* Présentationnel car tout ce qu'ils font est de générer des éléments d'interface utilisateur

Mais n'oubliez jamais que tout ceci se passe avant le développement avec React 16.8.
Pour l'instant, tous les composants fonctionnels peuvent faire les mêmes choses que les composants basés sur des classes.

```
import React from "react";
const Greeting = () => <h1>Hello World from my first component!</h1>;
export default Greeting;
```
