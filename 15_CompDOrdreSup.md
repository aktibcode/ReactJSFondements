# Chapitre : COMPOSANTE D'ORDRE SUPERIEUR


# Qu'est-ce que HOC ?

Nous avons vu la fonction d’ordre supérieur en JavaScript, qui est une fonction qui accepte une autre fonction comme paramètre.

Eh bien, React clone et imite cette fonctionnalité avec un composant, ce qui nous donne la possibilité de créer un composant d'ordre supérieur qui est un composant qui accepte un composant comme paramètre.

### Essentiellement, un composant d’ordre supérieur est une fonction qui prend un composant et renvoie un nouveau composant.

![](https://i.imgur.com/welsxVw.png)

# Pourquoi HOC?

Dans le développement de logiciels, il existe un principe important qui est communément utilisé sous le nom de « DRY » (qui signifie « Don't Repeat Yourself »).

Créer une fonction utilitaire simple, utilisée dans plusieurs parties de la base de code, est une opération que vous avez peut-être déjà effectuée à plusieurs reprises. En procédant ainsi, vous suivez essentiellement le principe DRY. Vous réutilisez la même fonction utilitaire, sans répéter le code.

Dans React, l’une des façons de suivre la méthode « DRY » dans les composants est d’utiliser le concept de composant d’ordre supérieur (HOC). Nous pouvons partager des fonctionnalités communes sans répéter le code.

# Exemple de HOC

Dans cet exemple, nous allons ajouter un message d'attente sur le composant encapsulé. Ne vous laissez pas trop submerger par ce code étrange. Nous le décomposerons plus tard.

```
import React from "react";

const higherOrderComponent = WrappedComponent => {
 class HOC extends React.Component {
   state = {
     isLoading: false
   };

   render() {
     return this.state.isLoading ? (
       <h1>Wait a moment...</h1>
     ) : (
       <WrappedComponent />
     );
   }
 }

 return HOC;
};
```
