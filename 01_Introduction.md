# **Chapitre : INTRODUCTION A REACTJS**

* Introduction

ES6 est une étape majeure dans l'évolution de JavaScript.

Après l'essor d'ES6, de nombreuses bibliothèques et frameworks sont apparus. React.js est considéré comme l'un des plus populaires.
C'est la raison pour laquelle nous avons choisi de nous concentrer sur l'apprentissage de React dans cette super compétence.

Au cours de cette super compétence, nous allons :

* Explorez React.js et comprenez les raisons de sa popularité.
* Apprenez à configurer un environnement afin que nous puissions commencer à utiliser React.js dès que possible.
* Découvrez comment démarrer avec React.js et faire nos premiers pas.

## Qu'est-ce que React ?

Comme nous l’avons dit précédemment, React.js est une bibliothèque JavaScript permettant de créer des interfaces utilisateur.

Vous vous demandez peut-être maintenant : **qu'est-ce qu'une bibliothèque ? Comment pouvons-nous la définir ?**

Une bibliothèque peut être définie comme un ensemble de fonctions et de classes regroupées dans un package.
L'idée principale derrière les bibliothèques est de créer un code réutilisable que n'importe quel membre de la communauté de développement peut utiliser et auquel il peut contribuer.

    https://youtu.be/3Nv9brpYSQE?list=PL-w_yrNy8uTaWNAYCFoyW0C0zPm4S9b3v

Si vous recherchez « Qu'est-ce que React.js ? » sur Google, vous trouverez des centaines d'articles informatifs et complets sur React.js. Mais nous sommes là pour vous aider à rester concis et precis.

React.js est une bibliothèque JavaScript open source utilisée pour créer des interfaces utilisateur spécifiquement pour les applications à page unique.

Il s'agit de gérer la couche de visualisation pour les applications Web et mobiles.

    https://dwglogo.com/wp-content/uploads/2017/09/1460px-React_logo.png

## Qu'est-ce qu'une application monopage ?

Les applications modernes ont tendance à adhérer à ce que l’on appelle un modèle d’application monopage (SPA = Single Page Application).

Dans notre navigation quotidienne, nous ne chargeons jamais de pages entièrement nouvelles et différentes, même si nous rechargeons la page. Au lieu de cela, les différentes vues de votre application sont chargées et déchargées de manière dynamique, écrites et réécrites dans la même page.

Le composant App.js sera le point de départ de notre SPA. App.js est le composant principal.

    https://youtu.be/BscORJBwrqY?list=PL-w_yrNy8uTaWNAYCFoyW0C0zPm4S9b3v


## Pourquoi utiliser React ?

Souvent, dans les applications du monde réel, le développement d'un site Web à l'aide de HTML, CSS et JavaScript peut s'avérer très difficile et monotone. Voici pourquoi :

* Vous devez créer manuellement des fichiers HTML, CSS et JavaScript pour chaque page de site Web.
* Si vous souhaitez déplacer un élément qui existe dans la page A vers une autre page B, vous devrez copier tout son HTML, CSS et JavaScript pour le faire fonctionner et cela est non seulement fastidieux mais aussi chronophage.
* Le partage de CSS et de JavaScript peut rendre la maintenance très difficile à mesure que le site Web se développe.

Pour résoudre les problèmes mentionnés précédemment, des bibliothèques et des frameworks ont heureusement vu le jour. Ils rendent le développement Web beaucoup plus facile et plus pratique pour les développeurs. L'une des principales solutions est React.js.


### Pourquoi devrions-nous choisir d'apprendre React.js ?

La réponse à cette question est très simple, React est :

* Facile à apprendre.
* Très facile à entretenir.
* Super rapide dans le rendu des vues.
* Basé sur des composants, avec la possibilité de diviser le code autant que nous le souhaitons
* Simple dans le processus de débogage.


## Caractéristiques de React :

React possède plusieurs excellentes fonctionnalités qui sont très utiles lors de la création de l'interface utilisateur.

    https://i.imgur.com/rdTeXr5.png


* **JSX** : React utilise la syntaxe JSX dans l'écriture des composants, ce qui les rend plus indépendants.
* **Composant** : React adopte l’approche d’application basée sur les composants qui nous permet d’utiliser le même composant à plusieurs reprises.
* **Flux de données unidirectionnel** : React nous permet uniquement de transmettre des données du parent à l'enfant, ce qui est très utile pour tracer les données lors du débogage.
* **DOM virtuel** : React utilise le DOM virtuel qui rend le rendu de l'interface utilisateur ultra rapide.
* **Simplicité** : React est très simple à apprendre et à utiliser, surtout pour les nouveaux arrivants.


## Applications créées avec React

Le monde numérique est en constante évolution et change au moment où nous parlons. Dans un tel monde, il est certainement difficile de s'adapter aux tendances. Pourtant, c'est exactement ce que font les grandes entreprises technologiques du secteur. Les
principales applications comme Facebook, Instagram, Netflix et d'autres améliorent constamment leur expérience et s'adaptent aux nouveaux cadres et tendances.
Depuis peu, le bouche-à-oreille se répand autour de ReactJS et de ses fonctionnalités impressionnantes.
La preuve de sa popularité est mieux décrite par les applications qui utilisent ReactJS. Aujourd'hui, nous allons vous montrer la liste des applications les plus impressionnantes basées sur ReactJS.
La plupart d'entre elles sont : Facebook, Instagram, ADA, Netflix, Dropbox, Paypal, etc...

    https://i.imgur.com/Ekaqkem.png


### Exemple : les films Netflix.

Prenons un exemple pour mettre en évidence la différence entre le HTML normal et React.
Essayons de reconstruire la liste de films de Netflix en utilisant HTML, puis de la reconstruire en utilisant React. Nous comparerons les deux versions plus tard.

    https://i.imgur.com/leX96ZJ.png


### Exemple : films Netflix utilisant HTML

En utilisant HTML, nous nous retrouvons avec ce fouillis de code incompréhensible :

```


<div class="nm-content-horizontal-row">
 <ul class="nm-content-horizontal-row-item-container">
   <li class="nm-content-horizontal-row-item" role="menuitem">
     <a
       class="nm-collections-title nm-collections-link"
       href="https://www.netflix.com/tn-en/title/70079583"
       data-uia="collections-title"
     >
       <img
         class="nm-collections-title-img"
         src="..."
         data-title-id="70079583"
         alt="The Dark Knight"
       />
       <span class="nm-collections-title-img placeholder"></span>
       <span class="nm-collections-title-name">The Dark Knight</span>
     </a>
   </li>
   <li class="nm-content-horizontal-row-item" role="menuitem">
     <a
       class="nm-collections-title nm-collections-link"
       href="https://www.netflix.com/tn-en/title/80013871"
       data-uia="collections-title"
     >
       <img
         class="nm-collections-title-img"
         src="..."
         data-title-id="80013871"
         alt="American Sniper"
       />
       <span class="nm-collections-title-img placeholder"></span>
       <span class="nm-collections-title-name">American Sniper</span>
     </a>
   </li>
   <li class="nm-content-horizontal-row-item" role="menuitem">
     <a
       class="nm-collections-title nm-collections-link"
       href="https://www.netflix.com/tn-en/title/80064516"
       data-uia="collections-title"
     >
       <img
         class="nm-collections-title-img"
         src="...."
         data-title-id="80064516"
         alt="The Revenant"
       />
       <span class="nm-collections-title-img placeholder"></span>
       <span class="nm-collections-title-name">The Revenant</span>
     </a>
   </li>
 </ul>
</div>
```


### Exemple : films Netflix utilisant React.js

D'un autre côté, après avoir refactorisé ce code dans React à l'aide de composants, nous obtenons un code beaucoup plus propre.
Notez que `<Movie/>`la balise ne fait pas partie du HTML, c'est une balise que nous avons créée à l'aide de React. Cela s'appelle un **composant React** .


```
<Container>
 <Row>
   <Movie image={...} title=”The Dark Knight”
   href=”https://www.netflix.com/tn-en/title/70079583”/> <Movie image={...}
   title=”American Sniper”
   href=”https://www.netflix.com/tn-en/title/80013871”/> <Movie image={...}
   title=”The Revenant” href=”https://www.netflix.com/tn-en/title/80064516”/>
 </Row>
</Container>
```
