# Les raccourcis EMMET

- Ouvrir le doctype
````text
! + tab
````
- Balise link
````text
link + tab
````

- Pour les différentes balises
````text
balise + tab
````

- Générer du texte 
````text
lorem50 + tab #Génére 50 mots
````

- Ajouter des classes ou des id
````text
element.NomClasse #Donne une classe à un élément
element.NomClasse.NomClasse #Donne deux classe à un élément

element#id #Donne un id à l'élément
````

- Ajouter du contenu à l'intérieur d'un élément
````text
conteneur{Some text}
# Possible en ajoutant des classes
h1.title{titre} + tab
````

- Faire de l'imbrication
````text
div>ul>li>a
````

- Ajouter un élément de même niveau
````text
div>p+ul>li>a
````
- Multiplier les éléments 
````text
div>p+ul>li*2>a
````
- Faire de l'indexation avec les éléments avec $
````text
    ul>li.item.item$*5
````
Ce qui donne en HTML : 
````html
    <ul>
        <li class="item item1"></li>
        <li class="item item2"></li>
        <li class="item item3"></li>
        <li class="item item4"></li>
        <li class="item item5"></li>
    </ul>
````

- Monter d'un étage 
````text

````