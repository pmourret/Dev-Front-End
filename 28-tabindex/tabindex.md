# TABINDEX

- Permet de sélectionner l'ordre dans lequel les éléments peuvent être selectionnés à l'aide de la touche TABULATION

### Exemple

```html
<h1 tabindex="1">Un titre</h1>
<p tabindex="2">Lorem ipsum dolor sit amet....</p>
<button tabindex="3">Button 1</button>
<button tabindex="4">Button 2</button>
<button tabindex="5">Button 3</button>
```

- Il est possible d'ignorer un ou plusieurs élément(s)
````html
<h1 tabindex="1">Un titre</h1>
<p tabindex="-1">Lorem ipsum dolor sit amet....</p>
<button tabindex="3">Button 1</button>
<button tabindex="4">Button 2</button>
<button tabindex="5">Button 3</button>
````



