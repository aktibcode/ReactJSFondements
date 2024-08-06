# Chapitre :  ATTRIBUTS ET FICHIER POUR LE STYLE


# Attributs : style

Il est temps de pimenter vos éléments JSX !

Dans cette section, nous allons apprendre à styliser les éléments JSX. C'est légèrement différent du HTML normal.

* Voici quelques règles à garder à l’esprit :
* Apostrophes (') ou guillemets (“) sur les chaînes
* **camelCase** (Voir page suivante)
* Des virgules (,) au lieu d'un point-virgule (;)
* Deux **accolades {{}}** au lieu de **guillemets (« »)**

### **HTML**

```
<h1 style= "color:red; font-size:60px">
...
</h1>
```

---

### ---> **JSX**

```
<h1 style={{ color: "red", fontSize: 60 }}>...</h1>
```

# Qu'est-ce que camelCase ?

Vous vous demandez probablement ce qu'est CamelCase. Eh bien, nous avons les réponses.

> « Il s'agit d'écrire des phrases en un seul « mot » sans espaces. Nous l'utilisons pour écrire des noms de variables en JavaScript. »

Le concept est très basique. Il y a 2 règles simples à suivre :

1. Pas d'espaces, pas de traits de soulignement ( _ ) et pas de tirets (-)
2. Si la variable est composée de plusieurs mots, tous les mots commencent par une **majuscule** sauf **le premier mot** .

# Exemples

Voyons d'autres exemples de style.
Nous constatons fréquemment que la version HTML est ordonnée juste avant la version JSX.

---

### HTML

```
<div style='text-align:center'/>
```

### JSX

```
<div style={{textAlign:'center'}}/>
```

---

---

### HTML

```
<div style="transform:translateX(25px)"/>
```

### JSX

```
<div style={{transform:'translateX(25px)'}}/>
```

---

---

### HTML

```
<div style="box-shadow:0 5px 8px #000"/>
```

### JSX

```
<div style={{boxShadow:"0 5px 8px #000"}}/>
```

---

# Les unités de mesure dans JSX :

Certaines **propriétés CSS** peuvent prendre un nombre, elles auront par défaut **le px (pixels)** comme unité. Si vous devez spécifier une unité différente, vous devez utiliser le type chaîne.

---

### HTML

```
<div style=”height:10px”/>
```

### JSX

```
<div style={{height:'10px'}}/>
```

---

---

### HTML

```
<div style=”height:10px”/>
```

### JSX

```
<div style={{height:10}}/>
```

---

---

### HTML

```
<div style=”height:10vw”/>
```

### JSX

```
<div style={{height:'10vw'}}/>
```

---

# className

Une autre façon de styliser les éléments HTML consiste à utiliser les classes CSS. Dans JSX, pour utiliser la classe CSS, nous devons changer l'attribut **class** en **className** , car le mot-clé class est réservé en JavaScript.

### HTML

```
 <div class=”colorful”>...</div>
```

### JSX

```
<div className='colorful'>...</div>
```

# Attributs : fichier de style

Étant donné que les éléments JSX peuvent avoir des attributs comme des classes CSS, nous pouvons également utiliser les fichiers externes pour styliser ces éléments.
Essayez de créer un fichier appelé **style.css** .

### style.css

```
.my-profile{
 width:200px;
}
```

Ensuite, il ne vous reste plus qu'à importer le fichier comme ceci :

### JSX (en haut)

```
import "./styles.css";
```

Maintenant, créons la photo **de profil** et donnons-lui un nom de classe **my-profile** pour appliquer le style CSS.

### Application.js

```
function App() {
 let firstName = "Will";
 let lastName = "Smith";
 return (
   <div>
     <img src="/profile.png" className="my-profile" alt='Will Smith'/>
     <p>
       {firstName} {lastName}
     </p>
   </div>
 );
}
```
