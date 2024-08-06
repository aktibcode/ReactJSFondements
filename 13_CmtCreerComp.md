# Chapitre : COMMENT CREER DES COMPOSANTS


# Création de notre premier composant :

Après tout ce qui a été dit sur les composants, il est temps de se salir les mains.
Créons notre premier composant React !
Créer un composant est bien plus simple qu'on ne le pense. En pratique, un composant est simplement une fonction qui renvoie du JSX, c'est tout ce dont nous avons besoin pour créer un composant.
En utilisant la puissance de JavaScript, nous pouvons manipuler ces fonctions à notre guise. Nous allons créer le composant Greeting que nous avons vu auparavant. C'est très simple. Il suffit de suivre les instructions :

1. Créez le projet dans le dossier src,
2. Ouvrez l'App.js,
3. Ensuite, copiez-collez ce code.

```
import React from "react";
const App = () => {
 return (
   <>
     <h2>Hello from my first component !!</h2>
   </>
 );
};
export default App;
```

### Sortir

![](https://i.imgur.com/p8S91Q8.png)

Félicitations ! Vous avez créé votre premier composant. Et OUI ! L' **App.js** est également un composant. Nous le découvrirons plus en détail dans les prochaines diapositives.

# De quoi faut-il se souvenir ?

Il y a quelques points que vous devez remarquer à propos de ce premier exemple, le premier est que `import React from "react";`c'est obligatoire puisque nous travaillons avec JSX et que `export default App;`c'est aussi une action obligatoire qui doit être effectuée. Nous allons expliquer sa nécessité. Souvenez-vous du cours sur ES6 et de la façon dont il a rendu notre vie de développeur beaucoup plus facile. Il est temps de revenir en arrière et d'en profiter.

Afin de séparer les composants les uns des autres, nous devons utiliser la modularité JavaScript.

React nous donne également la possibilité d'utiliser les exportations nommées et les exportations par défaut

La dernière chose que vous devez remarquer est que le composant commence par une lettre majuscule. Cela est nécessaire pour ne pas le confondre avec de simples balises HTML.

# Exportation par défaut

Semblable au fichier JavaScript, nous pouvons exporter notre composant, comme le montre l'exemple ci-dessous, en utilisant le mot-clé `export default`.

```
const MyFirstComponent = () => {
 return (
   <>
     <h2>Hello from my first component !!</h2>
   </>
 );
};
export default MyFirstComponent;
```

En faisant cela, nous avons fait en sorte que le fichier **MyComponent.js** exporte automatiquement le composant MyFirstComponent.

# Exportations nommées

L'autre façon d'exporter un composant est d'utiliser l'exportation nommée. Regardons un exemple.

C'est ainsi que nous pouvons exporter plusieurs composants à partir d'un seul fichier.

```
import React from "react";
export const MyFirstComponent = () => {
 return (
   <>
     <h2>Hello from my first component !!</h2>
   </>
 );
};

export const MySecondComponent = () => {
 return (
   <>
     <h2>Hello from my second component!! </h2>
   </>
 );
};
```

# Bonnes pratiques pour la création d'un composant :

Après avoir créé notre premier composant, voici une liste de quelques bonnes pratiques courantes que nous devrions connaître :

* Gardez les composants petits et spécifiques à la fonction :
  * Les composants spécifiques à une fonction peuvent être autonomes, ce qui facilite les tests et la maintenance.
  * Chaque petit composant peut être réutilisé dans plusieurs projets.
  * Avec des composants plus petits, il est plus facile de mettre en œuvre des optimisations de performances.
  * Il est plus facile de mettre à jour des composants plus petits.
  * Les composants plus gros doivent être plus performants et peuvent être difficiles à entretenir.
* Nommez le composant d'après la fonction :
  *c'est une bonne idée de nommer un composant d'après la fonction qu'il exécute afin qu'il soit facilement reconnaissable.*
* Conservez-les tous dans un seul dossier :
  *conservez tous les fichiers relatifs à un composant dans un seul dossier, y compris les fichiers de style.*
* La réutilisabilité est importante.
