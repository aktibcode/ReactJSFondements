# Chapitre : TYPES DE PROPS


# Types de props

Les props sont un mécanisme très important pour transmettre des attributs en lecture seule aux composants React. Ces attributs doivent généralement être d'un certain type ou d'une certaine forme pour pouvoir être utilisés correctement dans le composant.

Si un prop est transmis à un composant dans un type ou une forme qui n'est pas familier, le composant peut ne pas se comporter comme prévu. Ainsi, une excellente façon d'améliorer les composants React est la validation des props.

### propTypes :

React fournit un mécanisme interne pour ajouter une vérification de type aux composants. Les composants React utilisent une propriété spéciale nommée **propTypes** pour configurer la vérification de type.

Lorsque des propriétés sont transmises à un composant React, elles sont vérifiées par rapport à la définition de type configurée dans la propriété **propTypes** . Lorsqu'une valeur non valide est transmise pour une propriété, un avertissement s'affiche sur la console JavaScript.

![](https://i.imgur.com/LT52g3a.png)

## React.PropTypes :

Avant React 15.5.0, un utilitaire nommé PropTypes était disponible, dans le cadre du package React, qui fournissait de nombreux validateurs pour configurer les définitions de type pour les propriétés des composants. Il était accessible avec **React.PropTypes** .

Cependant, dans les versions ultérieures de React (maintenant 18), cet utilitaire a été déplacé vers un package distinct nommé prop-types, vous devez donc l'ajouter en tant que dépendance pour votre projet afin d'accéder à l' utilitaire **PropTypes :**

```
npm install prop-types --save-dev
```

Il peut être importé dans vos fichiers de projet comme suit :

```
import PropTypes from "prop-types";
```

Vous pouvez l'utiliser comme suit :

```
/** FUNCTIONAL COMPONENTS **/
function ReactComponent(props) {
 // ...implement render logic here
}

ReactComponent.propTypes = {
 // ...prop type definitions here
};
```

## Validateurs PropTypes :

Comme indiqué dans la section précédente, l' `PropTypes`utilitaire exporte de nombreux validateurs pour configurer les définitions de type. Voici les validateurs pour les types de données de base :

`PropTypes.any // PropTypes.bool // PropTypes.number // PropTypes.string // PropTypes.func // PropTypes.array // PropTypes.object // PropTypes.symbol`

```
Component.propTypes = {
 anyProp: PropTypes.any,
 booleanProp: PropTypes.bool,
 numberProp: PropTypes.number,
 stringProp: PropTypes.string,
 functionProp: PropTypes.func
};
```

# Plusieurs types :

`PropTypes`nous exportons également des validateurs qui peuvent autoriser un ensemble limité de valeurs ou plusieurs ensembles de types de données pour une propriété. Les voici :

* **PropTypes.oneOf :** le prop est limité à un ensemble spécifié de valeurs, le traitant comme une énumération.
* **PropTypes.oneOfType :** l'accessoire doit faire partie d'un ensemble de types spécifié, se comportant comme une union de types.

```
Component.propTypes = {
 enumProp: PropTypes.oneOf([true, false, 0, "Unknown"]),

 unionProp: PropTypes.oneOfType([
   PropType.bool,
   PropType.number,
   PropType.string,
   PropType.instanceOf(Person)
 ])
};
```

# Accessoires requis :

Il arrive souvent que vous ayez besoin de contrôler la sortie de votre composant. Vous pouvez le faire grâce au rendu conditionnel.

Vous pouvez empêcher le composant de s'afficher lorsqu'un accessoire requis n'est pas transmis ou n'est pas valide en affichant une sortie alternative à la place. Cela se fait en utilisant le rendu conditionnel.

```
const SimpleComponent = ({ requiredProps }) => {
 return (
   <>
     {requiredProps ? (
       <h1>We need this {requiredProps} !</h1>
     ) : (
       <h1>Ooops ! we need that props</h1>
     )}
   </>
 );
};
```

Nous définissons une alternative pour notre sortie avec **requiredProps** .
