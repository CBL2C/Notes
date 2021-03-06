# Basic CSS Notes

CSS is short for Cascading Style Sheets.  
The "cascading" algorithm determines how CSS is applied to a web page. For now, know that CSS rules "cascade" down the page, and that rules farther down the document will overwrite the same rules above.

So if I have at the very top of my document on Line 1:
```css
body{
    background-color: green;
}
```
but on line 299, I have:
```css
body{
    background-color: red;
}
```
The page's ```background-color``` will be ```red```, because the rule on line 299 **overwrites** the rule on Line 1.
<br>

CSS determines the width, height, colors, margins, borders, backgrounds, etc. of web pages.  
CSS is **incredibly** powerful and **incredibly** flexible. Many times a difficult animation or transition that is assumed to be JS wizardry is actually just a good grasp of what CSS can do. 

<br>

## External and Internal Stylesheets
CSS may be applied to a web page using two methods: 
* External Stylesheets
* Internal Stylesheets

<BR>

### External Stylesheets
**External stylesheets are the preferred way to utilize CSS**  
External stylesheets are CSS documents that exist on their own, independent from any other code or HTML. They are easier to maintain and have the advantage of being modular.  
External stylesheets can also be linked to multiple HTML pages.
```css
stylesheet.css
```
External stylesheets are linked in HTML with ```link rel```:
```html
<link rel="stylesheet" href="CSS/Style.css">
```
<br>


### Internal Stylesheets
Internal stylesheets are placed in the ```<head>``` of an HTML document using ```<style>``` tags.  
Internal Stylesheets are sometimes still used, but in general it's seen as bad practice to internally style a page's CSS in ```<style>``` tags.  
**When in doubt, Use an External Stylesheet instead**
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">

    <style>
        body{
            background-color:#333333;
        }
    </style>

    <title>Some Web Page</title>
  </head>
```
<br>

### Inline Styles -- NO!
CSS styling *can* be applied directly to HTML elements... but please don't. **Please don't do this.**  
This example is presented solely because it's still semi-common to run into inline styling in the wild while looking at sites with dev tools, and it helps to know what you're looking at. 

Inline CSS Styling is the equivalent of a kid writing with crayon on the wall:  
You may have made it work, but no one is happy & now your mess needs cleaned up. 

**Do Not Do This:**
```html
<body>
    <--! Please Do Not Do This -->
    <section style="background-color:#333333;">     // NO!!
    <--! God No -->
    </section>
</body>
```


<br>

## CSS Selectors
<img src="../images/CSSRuleSet.png">


Every CSS rule starts with a selector, seen above in pink. These selectors often are the same or very similar to HTML Attributes that we have already covered, and reference those attributes. 

Common selectors include:
* element (type) selectors
* id selectors
* class selectors

<br>

### Element Selector
``` css
    h2 {
       font-family:monospace;
   }
```
<br>

### ```class``` Selector
```class``` selectors may be applied to multiple HTML elements.  
Multiple ```class``` selectors may be applied to a single element.
``` css 
    .redclass {
       color:red;
   }
```
<br>

### ```id``` Selector
```id``` selectors should be unique and only applied to one HTML element.  
If ```id``` is used multiple times, only the first element with that ```id``` will be targeted

Multiple ```id```s cannot be set on the same element
```css
    #bigdiv {
        background-color:red;
   }
```
```html
    <div id="bigDiv">
        <h2>Hello World</h2> 
        <h3 class="redclass">Red Red Red</h3>
    </div>
```
<br>

### Attribute Selector
```css
a[title]{                        // select all <a> tags that have a title
    font-size: 1.5 rem;
}
```
An attribute selector will search for an attribute *with the given selector inside* - in this example, the selector is searching for all ```<a>``` tags that also have a ```title``` inside the tag

<br>

## HTML ```<span>``` Element
The ```<span>``` element is an HTML element that allows you to drop a CSS class or id hook wherever you need with no unwanted side effects

```html
<head>
    <style>
        .red{
            color:red;
        }
    </style>
</head>
<body>
    <p>I wish this <span class="red">text was red</span></p>
</body>
```
<br>

## HTML ```<div>``` Element
The ```<div>``` element is an HTML element that allows you to separate your information into divided sections. Its primary features are the ability to give a ```<div>``` an ```id``` or ```class```
```css
<body>
<div class="first">Fiiiiirrrrstt!</div>
</body>
```
<br>

## Pixels vs. Em vs. Rem

```css
/* Pixels are not fixed across resolutions */
body{
    font-size:16px;
}


/* But em and rem are */
body{
    font-size:2em;
}

body{
    font-size:3rem;
}
```

Pixels do not render at the same size across different monitors:  
100px is going to look different at 1024px x 768px than it does at 2560px x 1440px.

Because of this, it is better to use ```em``` and ```rem``` than it is to use ```px```

### Em
```em``` is relative to the font size of its direct or nearest parent  
Because of this, ```em```'s size may fluctuate based on where in the page it is used


### Rem
```rem``` is relative to the root HTML document font size, so using ```rem``` will always scale to the same size across HTML elements

<br>