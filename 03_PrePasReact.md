# Démarrer un projet

Exécutons le projet et voyons à quoi ressemble notre application React. Nous devons d'abord :

1. Accédez au sous-dossier créé par **create-react-app** en utilisant la ligne de commande/Terminal.
2. Exécutez la commande suivante :

```
Desktop> cd myfirstapp
Desktop/myfirstapp> npm start
```

***Astuce** : cette commande exécutera le script nommé « start » dans le package.json.*

# Le résultat:

![](https://i.imgur.com/hIx4Gqt.gif)

La commande précédente ouvrira le navigateur contenant notre site Web React.

Maintenant, essayez de jouer avec le code HTML qui se trouve dans le fichier **App.js** que vous pouvez trouver dans le dossier **src** .

**Assurez-vous d'avoir une sauvegarde du `App.js`fichier.**


# La structure du projet :

Vous vous demandez peut-être pourquoi le projet React contient autant de dossiers et de fichiers. Nous ne les passerons pas tous en revue, mais nous devons comprendre le but de certains d'entre eux.
Nous pouvons diviser ces fichiers en deux sections.

1. fichiers liés à npm

* **node_modules**
* **package.json**

2. Fichiers liés à React

* **public**
* **src**

![](https://i.imgur.com/5KJeOXQ.png)

# Le registre npm :

![](https://i.imgur.com/hOUTIqx.png)

Comme vous pouvez le voir, **npm** joue un rôle important dans notre projet React.
Comme il s'agit d'un gestionnaire de paquets, il sera chargé d'installer tous les paquets dont notre projet a besoin, notamment : React, ReactDOM et autres.
Lors de la création de l'application React, npm récupérera tous ces paquets à partir du **registre npm** . Le registre contient tous les paquets publiés par les développeurs.

# Fichiers npm

* **Package.json :** un fichier contient tous les noms des packages/dépendances que nous installons dans notre projet et leurs versions exactes.

![](https://i.imgur.com/bbePcGI.png)

* **Node_modules :** un dossier contient toutes les dépendances installées dans le projet (y compris React).

***Astuce :** si nous supprimons accidentellement les nodemodules, nous pouvons toujours réinstaller les packages à partir du package.json.*

le **package.json** garde une trace de tous les packages que nous avons utilisés. En fait, lors du partage de projets, nous excluons le dossier node_modules.

# Fichiers React

* **Dossier public :** c'est là que nous allons placer toutes nos images, SVG, icônes et tous les éléments dont nous avons besoin pour notre projet.
  Ce dossier contient un **index.html.** Ce fichier est la première et la seule page HTML qui se charge lorsque nous accédons à notre site Web. C'est le point d'entrée de notre projet (il s'agit d'une application monopage ou SPA, comme celle que nous avons mentionnée il y a quelque temps).
* **Dossier src :** le dossier src contient notre code. Nous travaillerons sur ce répertoire la plupart du temps.

![](https://i.imgur.com/ZSq8FWq.png)
