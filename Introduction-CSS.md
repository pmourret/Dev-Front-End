# CSS :Les bases

## Sommaire : 
* [Introduction au CSS](#introduction-à-css-)
* [Ou écrire du CSS](#ou-écrire-du-css-)
* [Sélectionner des éléments en CSS](#sélectionner-des-éléments-en-css)
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