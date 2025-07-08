# Introduction à display: flex

La propriété CSS `display: flex` permet de créer des mises en page flexibles et réactives facilement. Elle s'applique à un conteneur pour organiser ses éléments enfants en ligne ou en colonne.

## Utilisation de base

Pour utiliser Flexbox, il suffit d'ajouter `display: flex` à un conteneur :

```css
.conteneur {
  display: flex;
}
```

### Exemple HTML

```html
<div class="conteneur">
  <div>Élément 1</div>
  <div>Élément 2</div>
  <div>Élément 3</div>
</div>
```

## Propriétés principales

- `flex-direction` : définit la direction (ligne ou colonne)
  - `row` (par défaut) : les éléments sont alignés en ligne
  - `column` : les éléments sont alignés en colonne
- `justify-content` : aligne les éléments sur l'axe principal (gauche, centre, droite, espace entre...)
- `align-items` : aligne les éléments sur l'axe secondaire (haut, centre, bas...)

### Exemple d'alignement

```css
.conteneur {
  display: flex;
  justify-content: center; /* centre horizontalement */
  align-items: center;     /* centre verticalement */
  height: 200px;
  border: 1px solide #ccc;
}
```

## Résumé

Flexbox est très pratique pour aligner et répartir facilement des éléments dans un conteneur, sans utiliser de float ou de positionnement complexe.
