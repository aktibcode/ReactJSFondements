# Chapitre : Compare HTML et JSX


# Introduction

Dans le chapitre précédent, nous avons fait de grands progrès et nous avons appris à créer une page Web en utilisant **HTML** , **CSS** et **JS** .
Dans ce chapitre, nous allons découvrir comment créer des éléments dans React, en utilisant **JSX** .
**JSX** est une extension de JavaScript et il est utile lorsque nous voulons produire des éléments React.

Nous passerons en revue ses fonctionnalités et son fonctionnement.

# Qu'est-ce que JSX ?

JSX est une extension de syntaxe de JavaScript généralement utilisée avec React pour décrire à quoi doit ressembler l'interface utilisateur.
JSX peut vous faire penser à un langage de template, mais il offre toute la puissance de JavaScript.

![](https://i.imgur.com/0hVUq6v.png)

# JSX et HTML

Si vous jetez un œil au **fichier App.js** qui se trouve dans le dossier src, vous trouverez une combinaison de **JavaScript** et **de HTML (une sorte de HTML)** .
À l'intérieur de la fonction **App** dans l'instruction « return », vous trouverez un code qui ressemble à **du HTML** . Notez que lorsque vous modifiez ce code, la page s'actualise automatiquement dans le navigateur. Cela s'appelle **Live Reload** ou **Hot Reload** .

![](https://i.imgur.com/8h9MH4v.png)

# JSX et HTML

Jetez un œil à la fonction **App** . Vous vous demandez probablement pourquoi le HTML est placé de manière maladroite à l'intérieur de JavaScript. Cette syntaxe de balise inhabituelle n'est **ni une chaîne ni du HTML** . Elle s'appelle **JSX** .

```
function App() {
 return (
   <div className="App">
     <header className="App-header">
       <img src={logo} className="App-logo" alt="logo" />
       <p>
         Edit <code>src/App.js</code> and save to reload.
       </p>
       <a
         className="App-link"
         href="https://reactjs.org"
         target="_blank"
         rel="noopener noreferrer"
       >
         Learn React
       </a>
     </header>
   </div>
 );
}
```

# Comment ça marche?

À première vue, JSX et HTML semblent très similaires, mais en réalité ils sont très différents. Travailler avec JSX rend la manipulation des éléments HTML beaucoup plus facile et plus efficace.

Étant donné que chaque site Web est construit avec HTML et que les navigateurs comprennent naturellement HTML et non JSX, vous vous demandez peut-être : quel est le lien entre JSX et HTML ?

***Astuce :** si vous inspectez le code source de la page Web de React dans votre navigateur, vous ne trouverez que du HTML et non du JSX.*

![](https://i.imgur.com/641rKKT.png)

Grâce à React, le JSX est transformé en HTML puis injecté dans un **élément HTML** (racine) de la page HTML bien connue, l' **index.html** .

Cette injection se produit en fait dans le fichier **index.js grâce à ****ReactDOM** . Ce processus ne se produit qu'une seule fois, car l' **application** est le seul composant racine dans notre cas (nous n'avons généralement besoin que d'un seul composant racine).

# Récapitulatif JSX et HTML :

Récapitulons

!

* L'injection d'un composant à l'intérieur d'un élément HTML s'appelle **rendu** .
* Dans React, nous n'avons généralement qu'un seul composant racine (appelé **App** ).
* Nous n'avons besoin que d'un seul **composant racine** pour créer un site Web React.
* Le composant racine **(App.js)** est le point d'entrée de **React** .
* Nous n'avons besoin que d'un seul fichier HTML appelé **index.html** dans n'importe quelle application à page unique (comme React).
* JSX est compilé et rendu à l'intérieur de l' **élément racine** dans **index.html** .

<iframe allowfullscreen="true" frameborder="0" src="https://www.youtube.com/embed/cJkuLL16K7M"></iframe>
