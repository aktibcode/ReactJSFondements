# Chapitre : UTILISATION DES PROPS


# Création de notre premier accessoire

Similairement à un attribut HTML, pour envoyer un props d'un composant parent à un composant enfant, nous ajoutons le props comme attribut dans le processus d'appel du composant. Voici un exemple pour mieux comprendre cela.

```
<Welcome name="Sara" />;
```

Un composant peut avoir un nombre illimité de props, ce qui signifie que nous pouvons passer autant de props que nous le souhaitons. Jetez un œil à cet exemple :

```
<Welcome name= 'Sara' lastName = 'Smith' Age='27'/>
```

Veuillez noter que les noms que nous donnons aux accessoires sont personnalisés.
Même si nous pouvons appeler les accessoires comme nous le souhaitons, il existe quelques bonnes pratiques à suivre :
le nom doit être significatif et significatif afin que les autres puissent comprendre la valeur des accessoires.
Utilisez des minuscules (par exemple isActive).
Gardez le nom court (< 50 caractères).

Les props doivent être descriptifs. Les props décrivent ce que fait un composant et non pourquoi il le fait. Une erreur courante consiste à nommer les props d'après l'utilisateur actuel ou l'environnement actuel. Par exemple :
hasSubmitPermission décrit l'autorisation de l'utilisateur et la raison de la variation, mais pas le composant lui-même. Un meilleur nom pourrait être hasSubmitButton.`<MyForm hasSubmitButton={user.canSubmit} />`

# Utilisation d'accessoires

Il est temps d'utiliser nos premiers props après les avoir créés !
La première chose à faire lors de l'utilisation de props est de les passer en paramètre à la fonction du composant.

```
// we always use the keyword props in the function parameter
const Welcome = props =>{
 return (
   <h1>
     `Hello`
   </h1>
 )
}
```

Nous pouvons utiliser n'importe quel nom de paramètre, mais par convention, nous utilisons le mot-clé **props** .

# L'objet accessoires

Si nous exécutons un console.log() sur les props reçus, nous trouverons le résultat suivant :

---

### Application.js

```
const App = () => (
 <div>
   <Welcome name="Sara" />
 </div>
);
```

### Bienvenue.js

```
const Welcome = props =>{
console.log(`props:`,props)
 return (
   <h1> welcome </h1>
 )
}
```

---

### Sortir

![](https://i.imgur.com/S55PXMk.png)

Comme nous pouvons le voir dans l'exemple ci-dessus, même si les accessoires ont été transmis sous forme de chaîne, ils sont toujours arrivés sous forme d'objet au composant enfant.

# l'objet accessoires

Dans la diapositive précédente, nous avons vu que les props arrivent toujours sous forme d'objet aux composants enfants.
Pour pouvoir les utiliser, nous devons les traiter comme un objet. Nous pouvons accéder à la valeur souhaitée en utilisant l' **accesseur de propriété dot.**

```
const Welcome = props =>{
console.log(`props:`,props)
 return (
   <h1> welcome {props.name}</h1>
 )
}
```

![](https://i.imgur.com/EBgKuSn.png)

# Règles des accessoires

Nous avons dit plus tôt que les props sont **immuables,** mais que se passe-t-il si nous essayons de changer leur valeur ?
Jetez un œil à l'exemple ci-dessous :

```
const Welcome = props =>{
console.log(`props:`,props.name)
props.name ='John'// try to change the value into 'John'
 return (
   <h1> Welcome {props.name}</h1>
 )
}
```

![](https://i.imgur.com/EBgKuSn.png)

Nous aurons le même résultat qu'avant, car les accessoires sont en lecture seule.

# Fonctionne comme des accessoires

Nous savons que les props peuvent contenir n'importe quel type de données JavaScript, mais qu'en est-il des fonctions ?
Bien sûr, nous pouvons passer une fonction en tant que props du parent à l'enfant. En fait, cette astuce est utilisée pour passer des données de l'enfant au parent. Ne paniquez pas, nous savons que React est un flux de données à sens unique, mais dans une application réelle, nous sommes obligés de prendre un certain temps pour faire passer les données de l'enfant au parent.
Pour rendre cela possible, nous tirons parti de la fonction. Voici un exemple de ce dont nous parlons.

### Application.js

```
const App = () => {
 const alertMyInput = name => alert(name);
 return (
   <div>
     <Welcome name="Sara" alertMyInput={alertMyInput} />
   </div>
 );
};
```

### Bienvenue.js

```
const Welcome = props => {
 console.log(`props:`, props.name);
 return (
   <button onClick={() => props.alertMyInput(`My name is James Brown `)}>
     ClickMe
   </button>
 );
};
```

![](https://i.imgur.com/5mYa7oy.png)

# Conclusion

Nous savons qu'il y a beaucoup de matière à assimiler, mais les points clés que nous devons retenir sont les suivants :

* Les accessoires sont des arguments transmis aux composants React.
* Les accessoires sont utilisés pour assurer la communication à l'intérieur de l'arborescence des composants.
* Les accessoires sont immuables car leur valeur ne peut pas être modifiée par le composant enfant.
* Les accessoires ne sont transmis que du parent à l'enfant.
