# Chapitre : COMPOSANTS - VUE D'ENSEMBLE


# Introduction aux composants

Jusqu'à présent, nous avons appris ce que sont React et **JSX** . Nous avons appris leurs fonctionnalités, leurs avantages et leurs limites. Ce sont de grands pas que nous avons faits, mais il y a beaucoup plus de choses intéressantes qui nous attendent !
Maintenant, nous allons en apprendre davantage sur l'une des fonctionnalités les plus importantes de React : 'component', nous allons donc voir :

* Qu'est-ce qu'un composant ?
* Comment créer un composant ?
* Quels sont les différents types de composants ?
* Comment utiliser un composant ?
* Qu'est-ce que HOC dans React ?

# Qu'est-ce qu'un composant ?

Tout d'abord, avant de commencer par définir le composant React, examinons la définition d'un composant.
En effectuant une simple recherche sur Google, nous rencontrons de nombreuses définitions compliquées, mais essayons de rester simples. Un composant est un morceau de code qui peut être réutilisé et conçu pour coopérer avec d'autres composants afin de créer une interface utilisateur.
Regardons l'image ci-dessous et voyons comment elle est structurée :

![](https://i.imgur.com/swdJvKH.png)

# Avantages de l'utilisation de composants

Travailler avec des composants facilite grandement le développement Web. Les raisons sont les suivantes :

* ### Réutilisabilité :

Chaque composant implémenté peut, voire doit, être réutilisé lors de la construction de notre application web.
Prenons l'exemple d'une barre latérale sur un tableau de bord, elle sera utilisée quelle que soit la page que nous afficherons.

* ### Maintenabilité :

Chaque composant est implémenté séparément des autres afin qu'il puisse être maintenu sans affecter les autres compositions de l'interface utilisateur.

* ### Indépendance de la plateforme :

En réalité, les composants Web sont construits à l'aide de HTML, CSS et JavaScript, ce qui en fait un outil multiplateforme.

* ### Confidentialité:

Étant donné que chaque composant est conçu pour fonctionner seul, cela garantit que son contenu est plus privé que le code partagé.

# Qu'est-ce qu'un composant React ?

Les composants sont les éléments de base de toute application React. Vous remarquerez qu'une application React typique en aura beaucoup.
En termes simples, un composant est une classe ou une fonction JavaScript qui accepte éventuellement des entrées, c'est-à-dire des propriétés ou des accessoires, et renvoie un élément React qui décrit à quoi doit ressembler une section de l'interface utilisateur (UI).

```
// My first component
const Greeting = () => <h1>Hello World from my first component!</h1>;
```

Il s'agit d'un composant fonctionnel (appelé Greeting) écrit à l'aide de la syntaxe de fonction fléchée d'ES6. Il ne nécessite aucun accessoire et renvoie une balise h1 avec le texte « Bonjour le monde depuis mon premier composant ! »
