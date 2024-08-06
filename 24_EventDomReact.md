# Chapitre : EVENEMENTS DOM DANS REACT


# Événements DOM

Faisons un voyage dans le passé et souvenons-nous des événements DOM :

* Les événements sur un site Web interagissent toujours avec le navigateur. Par exemple, un `mouse click`, `file loading`sur le navigateur ou `swiping the image left or right`.

La gestion des événements avec des éléments React est très similaire à la gestion des événements sur les éléments DOM. Il existe quelques différences syntaxiques :

* Les événements React sont nommés en utilisant **camelCase** plutôt qu'en minuscules.
* Avec JSX, vous transmettez un nom de fonction comme gestionnaire d'événements plutôt qu'une chaîne.

Nous pouvons trouver de nombreux événements tels que **onMouseMove, onChange, onClick** et bien d'autres.

# Événements/Fonctions

Comme nous écrivons du JavaScript, les événements React sont écrits en syntaxe camelCase :
**onClick** au lieu de **onclick** .
Les gestionnaires d'événements React sont écrits entre accolades :
**onClick={handleClick}**

```
const ActionLink = () => {
 const handleClick = e => {
   e.preventDefault();
   console.log("The link was clicked.");
 };

 return (
   <a href="/" onClick={handleClick}>
     Click me
   </a>
 );
};
```

# Événements/Fonctions

Dans l'exemple ci-dessus, l' attribut **onClick** est notre gestionnaire d'événements et il est ajouté à l'élément cible afin d'assigner la fonction à exécuter lorsque cet élément est cliqué. L'attribut onClick est défini sur la fonction handleClick, qui envoie un message d'alerte.
En termes plus simples, cela signifie que chaque fois que le bouton est cliqué, la fonction handleClick est appelée et affiche la boîte d'alerte.

![](https://i.imgur.com/w2dmcka.png)

# Accessoires d'événements/fonctions

Il existe de nombreuses situations lorsque vous écrivez avec React et que vous souhaitez passer une fonction en tant que prop.
En général, il s'agit de la transmettre à un composant enfant afin que l'enfant puisse informer le parent d'un événement.
Dans cet exemple, nous avons passé la fonction handleClick du composant ActionLink en tant que prop à ActionComponent.
Nous attendons que ActionComponent déclenche une action, dans ce cas, il s'agit d'un message d'alerte.

![](https://i.imgur.com/G5aM38H.png)

# Test des accessoires des événements/fonctions

![](https://i.imgur.com/GIDspIE.png)

Dans ActionComponent, ce que nous attendons lorsque nous cliquons sur le lien Click Me! est d'envoyer un message d'alerte depuis handleClick qui est défini dans le composant parent ActionLink.

# Test des accessoires des événements/fonctions

![](https://i.imgur.com/FdI42LQ.png)

Comme prévu, l’alerte se déclenche et le test est réussi avec succès !

# Événements/Conclusion

La gestion des événements est un aspect très important à apprendre.
Étant donné que les applications sont basées sur les interactions des utilisateurs, la gestion nous donne le pouvoir de contrôler toute interaction qui se produit entre l'utilisateur et notre application.
React met en avant tous les gestionnaires d'événements DOM qui existent, avec seulement une petite différence dans la façon dont nous les appelons (l'utilisation de la dénomination camel case).
