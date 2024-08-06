# Chapitre : DECLARATION DES VARIABLES


# Exemples de base

**HTML**

```
<p id=”my-name”></p>
```

**JavaScript**

```

let firstName = 'Will';
let lastName = 'Smith';
document.getElementById('my-name').innerHTML = firstName + ' ' + lastName;
```

---

**JSX**

```

let firstName = "Will";
let lastName = "Smith";

return <p>{firstName + " " + lastName}</p>;
```

Pour utiliser une expression (opération ou variable) dans JSX, il vous suffit d'ajouter **des accolades {}** .

# Type JSX

Comme nous l'avons déjà établi, JSX consiste à écrire du HTML à l'intérieur de fichiers JavaScript, il peut donc hériter automatiquement de la puissance de JavaScript.
En JavaScript, nous pouvons affecter presque tout à une variable. De même, lorsque nous utilisons JSX, ce fait reste valable. Nous pouvons créer un élément JSX et l'affecter à une variable. L'exemple ci-dessous l'expliquera plus en détail :

```
function App(){
let input = (<input type='text' placeholder='Name'/>);
let button = <button>Submit</button>;
let form = (
  <form>
    {input}
    {button}
  </form>
);

return form;
}
```

# Type JSX

Comme JSX peut être stocké dans une variable, cela signifie qu'il peut également le renvoyer dans une fonction.
Voici comment procéder :

```
function App() {
 // We can put functions inside other functions when they are related
 function createForm() {
   let input = <input type="text" placeholder="Name" />;
   let button = <button>Submit</button>;
   return (
     <form>
       {input}
       {button}
     </form>
   );
 }
 return <div>{createForm()}</div>;
}
```

# Fonction d'appel

### **HTML**

```
<p id=”my-age”></p>
```

### **JavaScript**

```
document.getElementById(“my-age”)
       .innerHTML= getAge(1996)
```

---

### **JSX**

```
<p>{getAge(1996)}</p>
```

Si vous devez appeler une fonction (n'importe quelle fonction), vous pouvez le faire en l'appelant entre **accolades {}** .
Remarque : nous n'avons pas déclaré la fonction getAge() pour des raisons de simplicité.
