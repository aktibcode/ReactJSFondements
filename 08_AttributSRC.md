# Chapitre : ATTRIBUT SRC


# Attributs : src

L' `src`attribut est également disponible en JSX mais il est légèrement différent du HTML. Il existe plusieurs façons d'attribuer une valeur à l'attribut src.

## Chaîne codée en dur (pas une variable)

---

### HTML

```
<img src=“/profile.png”></img>
```

### JSX

```
<img src={"/profile.png"} alt="profile" />
 {/*  or we can also do */}
<img src="/profile.png" alt="profile" />
```

---

## Variable (peut être un nombre, un objet, un tableau, etc...)

---

### HTML

```
// We need DOM functions to do it
// like setAttribute()
```

### JSX

```
<img src={myProfileImageUrl}></img>
```

---

Les attributs dans JSX sont très similaires à ceux de HTML. Il suffit de remplacer les guillemets ("") par **des accolades {}** .

# Ajout d'une image

![](https://i.imgur.com/7xXnXTc.png)

Pour afficher une image sur la page, nous utilisons la balise `<img/>`.
Cette balise nécessite un attribut **src** , c'est le chemin vers l'image. Dans React, ce chemin peut être défini de deux manières, selon le répertoire dans lequel se trouve l'image :

1. 📁 annuaire **public**
2. 📁 répertoire **src**

# 📁 L'annuaire « public »

Si vous ajoutez l'image dans le répertoire **public** 📁 , vous devez la référencer dans l' attribut **src** avec une URL absolue (sous forme de chaîne).

**Conseils**

* Assurez-vous d'ajouter la barre oblique « / », elle s'appelle la racine.
* Si votre image se trouve dans un **sous-dossier** appelé 📁images dans le dossier 📁public, vous devez le spécifier
  * `<img src=”/subfolder/myImage.png”/>`

### JSX

```
<img src="/myImage.png" alt="myimage" />
```

# 📁Le répertoire « src »

Si vous ajoutez l'image dans le répertoire 📁 **src** , vous devez **l'importer** (en utilisant un chemin relatif vers src) puis **la définir** dans l' attribut **src de la balise ****`<img/>`** .

***Conseils***

* *Ajoutez le point « . » et la barre oblique « / » lors de l’importation d’une image dans src.*

JSX

```
import myWonderfulImage from "./myImage.png"
   function App(){
   return <img src={myWonderfulImage} alt ='myImage' />
   }
```

# Plus de conseils:

Éléments à garder à l’esprit lors de l’importation de l’image à l’aide de « import » :

* Si votre image se trouve dans le même dossier que votre fichier actuel :
  * ./monImage.png
* Si votre image se trouve dans le dossier parent :
  * ../monImage.png
* Si votre image se trouve dans un sous-dossier :
  * ./sous-dossier/monImage.png

### JSX

```
import myWonderfulImage from "./myImage.png"
```
