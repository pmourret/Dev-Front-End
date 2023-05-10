# CSS :Les bases

## Sommaire : 
* [Introduction au CSS](#introduction-à-css-)
* [Où écrire du CSS](#ou-écrire-du-css-)
* [Sélectionner des éléments en CSS](#sélectionner-des-éléments-en-css)
* [Les couleurs](#les-couleurs)
  * [Appliquer une couleur à un texte](#appliquer-une-couleur-à-un-texte-)
  * [Appliquer une couleur à un fond](#appliquer-une-couleur-à-un-fond)
* [Les dimensions](#les-dimensions)
  * [Les unités de mesure 1](#les-unités-de-mesure)
* [Les marges](#les-marges)
  * [Margin](#margin-)
  * [Padding](#padding)
* [Elements block et inline](#les-éléments-block-et-inline)
* [Les displays](#les-displays)

## Introduction à CSS 

* CSS signifie Cascading Style Sheets
  * Langage de feuille de style
  * Décrit et formate l'apparence d'un site ou application web
* Permet la séparation des données
  * HTML dans un fichier
  * CSS dans un fichier
* Peut être utilisé pour : 
  - Définir la couleur
  - Définir la police
  - Définir l'espacement
  - Définir la mise en page
  - etc
* Permet également d'ajouter :
  - Transitions
  - Animations
  - Des états
  - etc
## Ou écrire du CSS ?
* Directement dans une balise HTML : **style inline**
> :warning: Cette manière de faire est à éviter 
```html
<h1 style="color: red">style inline</h1>
```
* Au sein d'une balise style : **balise style**
> :warning: Cette manière de faire est à éviter
````html
<style>
  h2 {
    color: orange;
  }
</style>
<h2>Titre orange</h2>
````
* Dans une feuille de style : **style.css**
> :heavy_check_mark: Best practice !
````css
/* style.css */
h3 {
  color: blue;
}
````
````html
<!-- index.html -->
<link href="style.css" rel="stylesheet" type="text/css">

<h3>Titre bleu</h3>
````
## Sélectionner des éléments en CSS
* Directement par la balise
````css
p {
  color: red;
}
````
* Par la classe d'un élément
````css
.class {
  color: violet;
}
````
* Par l'ID d'un élément
````css
#id {
  color: green;
}
````
> :bulb: Bon à savoir : \
> Un élément ne posséde qu'un seul ID qui est unique à la page.\
> Un élément peut appartenir à plusieurs classes et une classe accepte plusieurs éléments.
### :warning: Régle importante en CSS
> Nom des éléments(balises) < Classes < ID < KEYWORD : important
````css
/* KEYWORD : important */
p{
  color: red!important;
}
````
* En ciblant les éléments enfants
````css
/* style.css */
.container p{
  color: crimson;
}
````
````html
<link rel="stylesheet" href="style.css" type="text/css">
<div class="container">
  <p>
    Lorem ipsum dolor sit amet.
  </p>  
  <p>
    Lorem ipsum dolor sit amet.
  </p>  
  <p>
    Lorem ipsum dolor sit amet.
  </p>
</div>
````
## Les couleurs

Il existe différentes méthodes pour appliquer une couleur en CSS :
- Par un nom prédéfini
````css
p{
    color: red;
}
````
- Par une valeur hexadécimale
````css
p{
    color: #8be9fd;
}
````
- Par un méthode rgb()
````css
p{
    /* rgba -> 'a' définit le canal alpha (opacité)  */
    color: rgba(125,12,46,1);
}
````
- Par une méthode hsl()
````css
/*
 * h -> hue = teinte
 * s -> saturation
 * l -> luminosity
 */
p{
    color: hsl(39, 100%, 50%);
}
````
### Appliquer une couleur à un texte 

````css
p{
  color: red;
}
````

### Appliquer une couleur à un fond

````css
p{
  background-color: orange;
}
````

## Les dimensions

Il existe différents attributs en CSS permettant de dimensionner des éléments.
````css
.container {
  /* Largeur de l'élément */
  width: 100px;
  /* hauteur de l'élément */
  height: 100px;
  
  /* Largeur maximale de l'élément */
  max-width: 75px;
  /* Largeur minimale de l'élément */
  min-width: 20px;
  
  /* Hauteur maximale de l'élément */
  max-height: 75px;
  /* Hauteur minimale de l'élément */
  min-height: 20px;
}
````
### Les unités de mesure
Il existe également différentes unités de mesure en CSS 

|     Unité     | Relative à                                                                          |
|:-------------:|:------------------------------------------------------------------------------------|
|      em       | La taille de police de l'élément                                                    |
|      rem      | La taille de police de l'élément racine                                             |
|       %       | La taille de l'élément parent                                                       |
|      px       | Une valeur en pixel                                                                 |
| Plus d'info.. | [Lien vers MDN](https://developer.mozilla.org/fr/docs/Web/CSS/CSS_Values_and_Units) |

## Les marges

Il existe deux types de marge en CSS :

### MARGIN 
  - Marge extérieure à l'élément
````css
.box{
    /* Marge extérieure supérieure */
    margin-top: 10px;
    /* Marge extérieure inférieure */
    margin-bottom: 10px;
    /* Marge extérieure gauche */
    margin-left: 10px;
    /* Marge extérieure droite */
    margin-right: 10px;
    
    /* Toutes les marges extérieures */
    margin: 10px;
    
    /* Deux valeurs : 
     * (supérieure + inférieure) 
     * (gauche + droite)
     */
    margin: 10px 15px;
    
    /*
     * Trois valeurs : 
     * supérieure
     * (gauche + droite)
     * inférieure
     */
    margin: 10px 15px 20px;
    
    /*
     * Quatre valeurs : 
     * supérieure
     * droite
     * inférieure
     * gauche
     */
    margin: 10px 20px 15px 5px ;
}
````
### PADDING
  - Marge intérieure à l'élément
````css
.box{
    /* Marge intérieure supérieure */
    padding-top: 10px;
    /* Marge  intérieure inférieure */
    padding-bottom: 10px;
    /* Marge intérieure gauche */
    padding-left: 10px;
    /* Marge intérieure droite */
    padding-right: 10px;
    
    /* Toutes les marges intérieures */
    margin: 10px;
    
    /* Deux valeurs : 
     * (supérieure + inférieure) 
     * (gauche + droite)
     */
    margin: 10px 15px;
    
    /*
     * Trois valeurs : 
     * supérieure
     * (gauche + droite)
     * inférieure
     */
    margin: 10px 15px 20px;
    
    /*
     * Quatre valeurs : 
     * supérieure
     * droite
     * inférieure
     * gauche
     */
    margin: 10px 20px 15px 5px ;
}
````

> :bulb: Astuce pour centrer un élément sur l'axe X 

````css
.box{
    background-color: salmon;
    width: 150px;
    height: 150px;
    /* RAPPEL : (superieur + inferieur) et (gauche + droite) */
    margin: 0 auto;
}
````

## Les éléments block et inline
En HTML il existe deux grandes familles d'éléments.
* Les éléments block 
  * Acceptent une grande partie des propriétés CSS
* Les éléments inline
  * N'acceptent pas les propriétés suivantes :
````css
span{
    width: 50px;
    height: 50px;
    margin-top: 25px;
    margin-bottom: 25px;
}
````
 * Mais acceptent les propriétés suivantes :
````css
span{
    margin-left: 25px;
    margin-right: 25px;
    padding: 15px; /* Toutes les marges intérieures */
}
````

## Les displays
