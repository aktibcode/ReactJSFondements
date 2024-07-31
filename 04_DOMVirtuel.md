# Chapitre : DOM VIRTUEL


# Introduction

Pour comprendre comment le concept de DOM virtuel est né, revenons brièvement sur le DOM.
Ce document peut être représenté par l'arbre DOM suivant :

![](https://i.imgur.com/I4hiB57.png)

# Le V.DOM

React gère deux DOM virtuels à la fois, l'un contient le DOM virtuel mis à jour et l'autre qui n'est que la version pré-mise à jour.

Maintenant, il compare la version pré-mise à jour avec le DOM virtuel mis à jour et détermine exactement ce qui a changé dans le DOM.

Ce processus est connu sous le nom de « diffing ». Une fois que React découvre exactement ce qui a changé, il met à jour uniquement les objets affectés sur Real DOM.

Cela améliore considérablement ses performances et c'est la principale raison pour laquelle Virtual DOM est apprécié par les développeurs du monde entier.

![](https://i.imgur.com/DtVVpkk.gif)

# Explication de ReactDom

ReactDOM est un package qui fournit des méthodes spécifiques au DOM, il peut être utilisé au niveau supérieur d'une application Web pour permettre une gestion efficace des éléments DOM de la page Web.

# React et le DOM virtuel

<iframe allowfullscreen="true" frameborder="0" src="https://www.youtube.com/embed/zdHGmCAbYQ4?list=PL-w_yrNy8uTaWNAYCFoyW0C0zPm4S9b3v"></iframe>

# La méthode de rendu :

ReactDOM fournit aux développeurs une API contenant les méthodes suivantes et bien plus encore.
Cette méthode peut prendre un maximum de trois paramètres comme décrit ci-dessous.

* **élément :** ce paramètre attend qu'une expression JSX ou un élément React soit rendu.
* **conteneur :** ce paramètre attend que le conteneur dans lequel se trouve l'élément soit rendu.
* **callback :** il s'agit d'un paramètre facultatif qui attend une fonction qui doit être exécutée une fois le rendu terminé.

![](https://i.imgur.com/anbemeT.png)
