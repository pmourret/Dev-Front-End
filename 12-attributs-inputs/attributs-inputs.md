# Les attributs des balises input

## Fonctionnant avec tous les types d'input

### **disabled**
- désactiver un input
```html
<input type="text" disabled>
```
### **autocomplete**
- indication de remplissage automatique
```html
<input type="text" autocomplete>
```

### **name**
- Libellé pour le back-end
```html
<input type="text" name="">
```

### **value**
- ajouter une valeur à l'input
```html
<input type="text" value="">
```

### **placeholder**
- Indication dans l'input pour l'utilisateur
```html
<input type="text" placeholder="indication">
```

### **required** 
- Rend le champ obligatoire
```html
<input type="text" required>
```

## Avec inputs particuliers

### **checked**
- Rend l'input déjà coché
#### CHECKBOX
```html
<input type="checkbox" checked>
```

#### RADIO
```html
<input type="radio" checked>
```

### **min**
- Définit une valeur minimale
#### RANGE
```html
<input type="range" min="0">
```
#### NUMBER
```html
<input type="number" min="0">
```
### **max**
- Définit une valeur maximale
#### RANGE
```html
<input type="range" max="10">
```
#### NUMBER
```html
<input type="number" max="10">
```
### **value**
- Définit une valeur par défaut
#### RANGE
```html
<input type="range" value="10">
```
#### NUMBER
```html
<input type="number" max="10">
```
### **multiple**

#### FILE

```html
<input type="file" multiple>
```

### **capture**

#### FILE
```html
<input type="file" capture>
```

## Avec les inputs de type image

### capture
```html
<input type="image" capture src="" alt="">
```