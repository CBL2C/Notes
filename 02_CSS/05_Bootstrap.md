# CSS Using Bootstrap
## What is Bootstrap?
Bootstrap is a giant collection of handy, reusable bits of code written in HTML, CSS, and JavaScript. It’s also a frontend development framework that enables developers and designers to quickly build fully responsive websites.

Essentially, Bootstrap saves time by avoiding writing lots of CSS, giving back time to spend on designing webpages.

**Bootstrap is popular because it has:**
* Responsive Grid
* Responsive Images
* Selected JQuery plugins
* Components:
    * Navigation bars
    * Dropdowns
    * Progress bars
    * Thumbnails 

<br>

## Responsive Grid
Grid Layout creates a  **12 column wide** grid-based layout system with rows and columns, making it easier to design web pages without having to use floats and positioning for CSS Box Model elements

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

<br>

### Grid Columns
<img src="../images/GridColumns.PNG">

### Grid Rows
<img src="../images/GridRows.PNG">
