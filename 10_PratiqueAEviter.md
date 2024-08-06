# Chapitre : PRATIQUE A EVITER


# Ne pas importer React

## Avant React V17

Lors de l'utilisation de JSX, la bibliothèque React doit être importée car les balises JSX sont compilées en instructions **React.createElement()** .

Si **React** n'est pas importé, une erreur se produira indiquant « Impossible de lire la propriété 'createElement' de undefined ».

### Application.js

```
import React from "react";

function App() {
 return <img src="/profile.png" className="my-profile" alt="myprofile" />;
}
```

## Mise à niveau de React V17 (et versions plus récentes) :

Après la publication de la 17e version de React, la bibliothèque a commencé à prendre en charge de nouvelles modifications JSX. Par conséquent, nous pouvons injecter la syntaxe JSX dans le fichier Javascript sans importer la bibliothèque React et cela fonctionnera sans problème.

```
function App() {
 return <img src="/profile.png" className="my-profile" alt="myprofile" />;
}
```

# Aucun nœud adjacent

L'une des erreurs les plus courantes commises dans JSX est l'utilisation de plusieurs éléments racines (lors du renvoi ou de la création de balises JSX). Il s'agit d'une limitation de JSX. Pour résoudre ce problème, nous devons utiliser une `<div>`balise vide ( `<></>`) ou `<React.Fragment>`.

*La mauvaise direction:*

```
 return  (
   <img src="/profile.png" className="my-profile" />
   <p>{firstName} {lastName}</p>
   )
```

*Le droit chemin:*

```
 return (
   <div>
     <img src="/profile.png" className="my-profile" alt="myprofile" />
     <p>
       {firstName} {lastName}
     </p>
   </div>
 );

 // or this way
 return (
   <>
     <img src="/profile.png" className="my-profile" alt="my profile" />
     <p>
       {firstName} {lastName}
     </p>
   </>
 );
// this is another way
 return (
   <React.Fragment>
     <img src="/profile.png" className="my-profile" alt="my profile" />
     <p>
       {firstName} {lastName}
     </p>
   </React.Fragment>
 );
```

# Utiliser la classe au lieu de className

L'utilisation de classes CSS dans JSX nécessite de définir l' `className`attribut, qui est différent de l' `class`attribut dans HTML. Cela a été fait exprès pour éviter tout conflit avec le mot-clé `class`dans les classes ES6.

*La mauvaise direction:*

```
 return  (
  <img src="/profile.png" class="my-profile" />
      )
```

*Le droit chemin:*

```
 return (
      <img src="/profile.png" className="my-profile" alt="myprofile" />
 );
```
