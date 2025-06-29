# CSS Grid - Guide Complet

## Introduction

CSS Grid est un système de mise en page bidimensionnel qui permet de créer des layouts complexes avec des lignes et des colonnes. Contrairement à Flexbox qui est unidimensionnel, Grid vous donne un contrôle total sur les deux dimensions.

## Concepts de Base

### 1. Container Grid vs Items Grid

- **Container Grid** : L'élément parent qui définit la grille
- **Items Grid** : Les éléments enfants qui sont placés dans la grille

### 2. Lignes et Colonnes

- **Lignes (Rows)** : Horizontales, numérotées de haut en bas
- **Colonnes (Columns)** : Verticales, numérotées de gauche à droite

## Propriétés du Container

### display: grid
```css
.container {
  display: grid;
}
```

### grid-template-columns
Définit le nombre et la taille des colonnes :
```css
.container {
  display: grid;
  grid-template-columns: 200px 200px 200px; /* 3 colonnes de 200px */
  grid-template-columns: 1fr 1fr 1fr; /* 3 colonnes égales */
  grid-template-columns: repeat(3, 1fr); /* Même chose que ci-dessus */
  grid-template-columns: 2fr 1fr 1fr; /* Première colonne 2x plus large */
}
```

### grid-template-rows
Définit le nombre et la taille des lignes :
```css
.container {
  display: grid;
  grid-template-rows: 100px 200px 100px; /* 3 lignes de tailles différentes */
  grid-template-rows: repeat(3, 1fr); /* 3 lignes égales */
}
```

### gap
Définit l'espacement entre les éléments :
```css
.container {
  display: grid;
  gap: 20px; /* Espacement uniforme */
  gap: 20px 10px; /* Ligne colonne */
  row-gap: 20px; /* Espacement entre lignes */
  column-gap: 10px; /* Espacement entre colonnes */
}
```

## Exemple Pratique - Layout de Base

```html
<div class="grid-container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
</div>
```

```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 100px);
  gap: 20px;
  background-color: #f0f0f0;
  padding: 20px;
}

.item {
  background-color: #3498db;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
  font-weight: bold;
}
```


## Fonctions Utiles

### repeat()
```css
.container {
  grid-template-columns: repeat(3, 1fr); /* 3 colonnes égales */
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); /* Responsive */
}
```



### fr (fraction)
```css
.container {
  grid-template-columns: 1fr 2fr 1fr; /* Proportions 1:2:1 */
}
```

## Exemple Avancé - Layout de Site

```html
<div class="site-layout">
  <header class="header">Header</header>
  <nav class="sidebar">Sidebar</nav>
  <main class="main">Main Content</main>
  <aside class="aside">Aside</aside>
  <footer class="footer">Footer</footer>
</div>
```

```css
.site-layout {
  display: grid;
  grid-template-areas: 
    "header header header"
    "sidebar main aside"
    "footer footer footer";
  grid-template-columns: 200px 1fr 200px;
  grid-template-rows: 80px 1fr 100px;
  min-height: 100vh;
  gap: 20px;
}

.header { 
  grid-area: header; 
  background-color: #2c3e50;
  color: white;
}

.sidebar { 
  grid-area: sidebar; 
  background-color: #34495e;
  color: white;
}

.main { 
  grid-area: main; 
  background-color: #ecf0f1;
}

.aside { 
  grid-area: aside; 
  background-color: #95a5a6;
  color: white;
}

.footer { 
  grid-area: footer; 
  background-color: #2c3e50;
  color: white;
}
```

## Alignement

### justify-items et align-items
```css
.container {
  justify-items: start | end | center | stretch; /* Alignement horizontal */
  align-items: start | end | center | stretch; /* Alignement vertical */
}
```

### justify-content et align-content
```css
.container {
  justify-content: start | end | center | stretch | space-around | space-between | space-evenly;
  align-content: start | end | center | stretch | space-around | space-between | space-evenly;
}
```

## Exercices Pratiques

### Exercice 1 : Grille Simple
Créez une grille 4x4 avec des éléments colorés.

### Exercice 2 : Layout de Blog
Créez un layout de blog avec header, sidebar, contenu principal et footer.

### Exercice 3 : Galerie d'Images
Créez une galerie d'images responsive qui s'adapte à différentes tailles d'écran.

## Bonnes Pratiques

1. **Utilisez des noms sémantiques** pour vos grid-areas
4. **Combinez Grid et Flexbox** pour des layouts complexes
5. **Testez sur différents navigateurs** (Grid est bien supporté)

## Support Navigateur

CSS Grid est supporté par tous les navigateurs modernes :
- Chrome 57+
- Firefox 52+
- Safari 10.1+
- Edge 16+

## Conclusion

CSS Grid est un outil puissant pour créer des layouts complexes et responsives. Avec de la pratique, vous pourrez créer des designs sophistiqués qui s'adaptent parfaitement à tous les écrans.

