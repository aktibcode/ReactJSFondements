# Chapitre : PROPS DE STYLE


# Accessoire de style

Il existe de nombreuses façons de styliser React avec CSS.
Nous allons examiner de plus près le style en ligne.

### Style en ligne :

Pour styliser un élément avec l'attribut de style en ligne, la valeur doit être un objet JavaScript :

![](https://i.imgur.com/P0xiHL3.png)

Noms de propriétés camelCase :
Étant donné que le CSS en ligne est écrit dans un objet JavaScript, les propriétés avec deux noms, comme text-align, doivent être écrites avec la syntaxe camel case : textAlign.

# Style en ligne

![](https://i.imgur.com/P0xiHL3.png)

Pour styliser un élément avec l'attribut de style en ligne, la valeur de l'attribut style doit être un objet JavaScript.

<div style={styleObject} > ou <div style={{color: “red”, textAlign: “center”}}>
Remarque : dans JSX, les expressions JavaScript sont écrites entre accolades, et comme les objets JavaScript utilisent également des accolades, le style dans l'exemple ci-dessus est écrit entre deux ensembles d'accolades {{}}.

# Conclusion

L'une des façons les plus simples d'ajouter du style au composant est d'utiliser un style en ligne. Par conséquent, il est préférable de garder à l'esprit que :

* Les règles CSS sont écrites en JavaScript, nous devons donc les modifier et suivre la norme JavaScript (camel case, sans espacement ni tirets).
* Le style est écrit dans un objet donc n'oubliez pas les doubles accolades.
