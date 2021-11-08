

# HTML Attributes
 


```html
<p id="welcome" class="placeholder" hidden>Lorem ipsum kitten doughnut french press suspenders lolcat</p>
```

**Attributes** can be added to the opening tags of HTML elements. 

An attribute typically has a name and a value. 

Above, the attribute name is ```id```, the attribute value is the string ```"welcome"```, and they are separated by an ```=``` equals sign.

Multiple atributes can be added to an HTML element by adding a space between attribute declarations. 

<br>

## Common Attributes
Some atttributes are more common to see than others on particular web pages, and some attributes have special behaviors that are worth knowing by heart

### ```id```
```html
<div id="profileCard">Some Div Content Here</div>
```
The ```id``` attribute is meant to be a **single, unique attribute** that is **not repeated on the page**.  
While you as a developer *can* choose to use multiples of the same ```id``` attribute for CSS use, this is **not advised**. 

Once you get into working with **JS**, it will become **extremely** important to follow the rule of only using **one unique ```id``` per ```id``` attribute** because **JS will only look for the first unique ```id``` attribute it finds and then stop.**   

So if you use more than one of the same unique ```id``` selectors while working with JS, you will run into problems. **Don't Do It.**

**Other Notes about ```id```:**
The value of ```id``` must:
* be a single string with no spaces.
* start with a letter
* use ```-``` hyphen or ```_``` underscore to connect multiple words in the string

<br>

### ```title```
The ```title``` attribute allows you to set a title for any HTML element on the page. This will set the element separate from the element the title is for in the HTML. 
```html
<p title="All About Dogs!">Lots of information about dogs here</p>
```
When the paragraph above is mouse-hovered, a tooltip appears with the title content inside:
<img src="../images/tooltip.PNG"> 

<br>

### ```class```


<br>

## Boolean Attributes
```html
<p hidden>Lorem ipsum kitten doughnut french press suspenders lolcat</p>
```

Some attributes will not have values, as they have their "true" state implied by existing in the tag. 

```hidden``` is one such attribute - by being present in the tag, the element is hidden. This element's existence implies its function is active. 

<br>
