# Chapitre : DESTRUCTURATION AVEC DES PROPS


# Réaffichage des changements d'accessoires.

Les composants React s'afficheront si les props changent. React exécute une comparaison entre les props nouvelles et précédentes et affichera automatiquement les nouvelles.
Nous avons ce composant React simple qui affiche le titre à l'écran :

```
import React from "react";

const MyComponent = ({ title }) => <h1>{title}</h1>;

export default MyComponent;
```

Nous allons simplement passer un props title au composant MyComponent :

```

<MyComponent title="I'm learning React" />;
//output on screen: I'm learning React
```

# Déstructuration avec des accessoires

Dans React, il est très courant de transmettre plusieurs props au composant. Il n'est donc pas étonnant que de nombreuses fonctions du composant React interagissent avec quelques props ou plus.

Voyons un exemple :

![](https://i.imgur.com/vTfG2Hm.png)

# Avantages de la déstructuration

Les avantages de l'affectation de déstructuration ES6 semblent encore plus nets dans le composant de fonction.

L'application de la technique de déstructuration des accessoires nous permet d'écrire du code comme celui-ci :

![](https://i.imgur.com/Ttbqy23.png)
