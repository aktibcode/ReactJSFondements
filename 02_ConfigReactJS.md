# Chapitre : CONFIGURATION DE REACT

## De quoi avans nous besoin ?

Assurez-vous d'avoir déjà installé ces outils, au cas où ce ne serait pas le cas.

1-	Node JS

Travailler avec npm (gestionnaire de paquets Node) et certaines bibliothèques liées à React nécessite NodeJS. Vous pouvez le télécharger ici : [https://nodejs.org/](https://nodejs.org/) .

![](https://i.imgur.com/cLvlQM5.png)

2-	Vsual Studio Code


2. ### Code de Visual Studio

Nous avons besoin d'un éditeur pour éditer les fichiers React. Vous pouvez télécharger VSCode ici : [https://code.visualstudio.com/download](https://code.visualstudio.com/download)

*Ou vous pouvez toujours utiliser votre IDE/éditeur préféré.*

![](https://i.imgur.com/lwKa9a1.png)


#### npx

Maintenant, nous allons créer notre premier projet React.
Les projets React nécessitent souvent quelques packages et une certaine configuration. Heureusement, il existe un package npm appelé **create-react-app** qui s'occupe de tout cela.
Nous pouvons appeler ce package directement sans l'installer grâce à la commande **npx** .


![](https://i.imgur.com/mGB5ItA.png)

![](https://i.imgur.com/A5V6wkP.png)

![](https://i.imgur.com/tiNc0k1.png)

![](https://i.imgur.com/CHb8kLJ.png)


## Créer une application réactive

Maintenant, nous allons créer notre projet en utilisant **create-react-app** et la commande **npx** .

Voici les étapes à suivre pour le faire :

1. Créons un dossier pour les projets React. Vous pouvez choisir n'importe quel dossier vide.
2. Accédez-y en utilisant la ligne de commande/Terminal.
3. Exécutez la commande suivante pour créer le projet React :
   **npx create-react-app `<project-name>`**
   ***Remarque** : remplacez  **`<project-name>`** par le nom de votre projet.*

Cette commande créera un sous-dossier nommé d'après le nom du projet que vous venez de spécifier.

```
~$ cd Desktop/
~/Desktop$ npx create-react-app myfirstapp
```
