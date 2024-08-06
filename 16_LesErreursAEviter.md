# Chapitre : LES ERREURS A EVITER


# Renvoyer plusieurs nœuds :

Étant donné que le composant n'est qu'une fonction JavaScript et que nous savons que les fonctions JavaScript ne peuvent renvoyer qu'un seul objet, valeur ou élément, le composant ne peut renvoyer qu'un seul élément JSX. Certes
, tout cela semble un peu trop compliqué. Voici la bonne façon de procéder.
Nous enveloppons tous les éléments sélectionnés dans un seul élément div ou section ou dans tout autre wrapper de notre choix. Jetez un œil à l'exemple ci-dessous.

```
const MyComponent = () => {
   // return multiple root node
   // WRONG!
   return (
    <Comp1 />
    <Comp2 />
   )
   }
   // this code will trigger an error
   // Parse Error: Adjacent JSX elements must be wrapped in an enclosing tag
```

### La bonne façon de le faire :

```
return (
 <div>
   <Comp1 />
   <Comp2 />
 </div>
);
```

# Fragment de réaction

Naturellement, le `div`ou `section`ou tout autre conteneur HTML ont intrinsèquement des propriétés CSS par défaut qui pourraient affecter notre conception.
Pour contourner ces propriétés par défaut, React nous fournit le **React.Fragment** qui est un wrapper qui n'a aucun effet sur le CSS. Un fragment React ne peut pas être stylisé.

Jetez un œil à sa syntaxe dans l’exemple fourni :

```
return (
 <React.Fragment>
   <div />
   <div />
 </React.Fragment>
);
//this also is valid
return (
 <>
   <div />
   <div />
 </>
);
```

# Utilisation de chemins absolus

L'utilisation d'un chemin absolu peut être un peu délicate et peut entraîner de nombreux problèmes lors de la tentative de réutilisation du composant.

⇒ Nous vous conseillons donc d’utiliser plutôt les chemins relatifs.

```
//relative path
import MyFirstComponent from "./MyFirstComponent";
//absolute path
import MyFirstComponent from '/src/component/MyFirstComponent'
```
