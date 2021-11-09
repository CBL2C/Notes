# CSS Grid
Grid Layout creates a grid-based layout system with rows and columns, making it easier to design web pages without having to use floats and positioning for CSS Box Model elements

## Grid Elements
### ```grid```
A grid layout contains a parent element with one or more child elements:
```html
<div class="grid-container">
  <div class="grid-item">1</div>
  <div class="grid-item">2</div>
  <div class="grid-item">3</div>
  <div class="grid-item">4</div>
  <div class="grid-item">5</div>
  <div class="grid-item">6</div>
  <div class="grid-item">7</div>
  <div class="grid-item">8</div>
  <div class="grid-item">9</div>
</div>
```

Now, to add CSS:
```css
.grid-container {
  display: grid;
}
```
Which makes:
<img src="../images/Grid1.PNG">
<br>

### ```inline-grid```
An Inline-Grid has the same HTML layout as above, but with a single CSS change:
```html
<div class="grid-container">
  <div class="grid-item">1</div>
  <div class="grid-item">2</div>
  <div class="grid-item">3</div>
  <div class="grid-item">4</div>
  <div class="grid-item">5</div>
  <div class="grid-item">6</div>
  <div class="grid-item">7</div>
  <div class="grid-item">8</div>
  <div class="grid-item">9</div>
</div>
```
```css
.grid-container {
  display: inline-grid;             // changed display from grid to inline-grid
}
```
And the results:

<img src="../images/Grid2.PNG">