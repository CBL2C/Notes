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
Grid Layout creates a **12 column wide** grid-based layout system with rows and columns, making it easier to design web pages without having to use floats and positioning for CSS Box Model elements

### ```grid```
A basic grid layout contains a parent element with one or more child elements. Here is a nine-column grid, with three columns per row:
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

**Grid Columns: a visual guide**  
<img src="../images/GridColumns.PNG">

**Grid Rows: a visual guide**  
<img src="../images/GridRows.PNG">


### Column Widths
Grid colums use the ```flex``` css selector. 
```css
.col
flex-basis: 0;
flex-grow: 1;
```

While ```.col``` is one selector for columns, there is also ```.col-1``` through ```.col-12```   

Notice how ```.col-4``` and ```.col-6``` behave:  
<img src="../images/GridColSizes.PNG">   
 ```.col-6``` has a built-in ```max-width``` of 50% of the available row space, while ```.col-4``` has a built-in ```max-width``` of 33% of the available row space

<br>


## Alerts
**[Alert Documentation](https://getbootstrap.com/docs/4.0/components/alerts/)**
Alerts provide contextual feedback messages for typical user actions.
```html
<div class="alert alert-primary" role="alert">
  This is a primary alert—check it out!
</div>
<div class="alert alert-secondary" role="alert">
  This is a secondary alert—check it out!
</div>
<div class="alert alert-success" role="alert">
  This is a success alert—check it out!
</div>
<div class="alert alert-danger" role="alert">
  This is a danger alert—check it out!
</div>
```

<img src="../images/AlertsBootstrap.PNG"><br>

Alerts can also provide links that are styled to match the alerts themselves
```html
<div class="alert alert-primary" role="alert">
  This is a primary alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-secondary" role="alert">
  This is a secondary alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
<div class="alert alert-success" role="alert">
  This is a success alert with <a href="#" class="alert-link">an example link</a>. Give it a click if you like.
</div>
```

<img src="../images/AlertsBootstrapLinks.PNG"><br>

Alerts can also contain additional HTML elements like headings, paragraphs and dividers

```html
<div class="alert alert-success" role="alert">
  <h4 class="alert-heading">Well done!</h4>
  <p>Aww yeah, you successfully read this important alert message. This example text is going to run a bit longer so that you can see how spacing within an alert works with this kind of content.</p>
  <hr>
  <p class="mb-0">Whenever you need to, be sure to use margin utilities to keep things nice and tidy.</p>
</div>
```

<img src="../images/AlertsBootstrapHTML.PNG"><br>

Please see **[Alert Documentation](https://getbootstrap.com/docs/4.0/components/alerts/)** the for how to dismiss alerts using the Jquery Plugin

<br>

## Breadcrumb

<br>

## Cards

<br>

## Carousel


