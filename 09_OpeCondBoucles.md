# Chapitre : OPERATEURS CONDITIONNELS ET BOUCLES

# Array Function map

L'une des meilleures fonctionnalités offertes par JSX est la possibilité d'utiliser l'itérateur pour restituer efficacement les éléments.

Supposons que nous ayons un tableau d'éléments que nous souhaitons afficher de la même manière, nous pouvons utiliser la méthode map pour le faire.

### HTML

```
<div id="list"></div>
```

### JavaScript

```
let arr = [1, 2, 3]
for (var i = 0; i < arr.length; i++) {
 append('<div>”+arr[i]+”</div>')
}
```

----->

### JSX (ES6)

```
{
[1, 2, 3].map(currentValue => (
       <div>{currentValue}</div>
))
}
```


### Après la compilation

```
<div>1</div>
<div>2</div>
<div>3</div>
```

# L'ancienne méthode

Le rendu des éléments avec des conditions est l'une des approches les plus vitales dans la création d'applications monopage (SPA). Heureusement, React nous donne la capacité de le faire parfaitement.

Jetons un œil à l’exemple ci-dessous :
disons que nous voulons afficher un formulaire indiquant que nous sommes ouverts tous les jours de la semaine sauf le dimanche.

### JSX

```
function App() {
 if (isSunday) {
   return <p>We are closed!</p>;
 }
 // the else is implicit (since the first case has a return
 return createForm();
}
```

***Remarque** : Gardez à l'esprit qu'il existe une meilleure façon de procéder. Nous la verrons dans un instant.*

# Opérateurs conditionnels avec JSX

Rappelons-nous et révisons l’opérateur logique en JavaScript.

### JavaScript

```
// AND
true && true // true
true && false // false
false && false // false

// OR
true  || true // true
true  || false // true
false || false// false

// Booleans from other types
!0  // true
!50 // false, since 50 !== 0
!""   // true
![] // false
!"hello"  // false, since “hello” !== “”
```

# Opérateurs conditionnels : ET/OU

L'opérateur logique `&&`and `||`peut être extrêmement pratique lorsqu'il s'agit de if implicite. Nous l'utiliserons dans JSX pour le simplifier. Lisez le code et les commentaires ci-dessous.

### JSX

```
 // Ask the user for a URL
let websiteUrl = prompt("Type in your URL");

location.href = websiteUrl;
// Redirects the user to the websiteUrl
// The problem with this example is that the user can leave the field empty (which means websiteUrl is // empty)

location.href = websiteUrl || 'http://google.com';
// Redirect the use to Google if it’s empty
// Now, if the user left the field empty, we will redirect him to Google. Otherwise he will be
// redirected to websiteUrl

// Or we can use the AND operator

websiteUrl && (location.href = websiteUrl);

// If the websiteUrl is not empty, redirect to it. Otherwise
// do nothing
```

# Opérateurs conditionnels : If/else avec JSX

L'opérateur logique `&&`et `||`sont très utiles lorsqu'il s'agit d' `if`une instruction simple, mais lorsqu'il s'agit d'une `if else`instruction, il est préférable d'utiliser l'opérateur ternaire.

```
// Ask the user for a URL
let websiteUrl = prompt("Type in your URL");

// Check if http exists in the url, add it otherwise
let protocolUsed = (websiteUrl.startsWith("https")) ? "https" : "http";

// Another example
(protocolUsed ==="https") ? alert("You are secure") : alert("You are not secure");
```

# Opérateurs conditionnels : expressions logiques

Revenons à JSX pour pouvoir appliquer **les opérateurs logiques** dans un scénario réel.
Le formulaire de cet exemple n'apparaît que lorsque le **firstName** est vide.

```
const firstName = prompt("type your first name");

 function App() {
   return (
     <div>
       <p> Hello {firstName || "Anonymous"} </p>
       <p> It looks like you {firstName ? "have" : "don’t have"} a name</p>
       {!firstName && (
         <form>
           <p> Type your name here </p>
           <input type="text" />
         </form>
       )}
     </div>
   );
 }
```
