# Page Structure & Layout

HTML is the most basic building block of the web.  
It provides the basic structure of a page's layout - text, media, ads, navigation, etc. 

<br>

**Page Structure:**

An HTML file is comprised of two basic components: 
* ```<head>```
* ```<body>``` 

A footer is also sometimes added on after the main body, but this is optional and is becoming less and less of a default for web developers. 

<br>

**Basic HTML File Boilerplate:**
```html
<!DOCTYPE html>                                   // Declaring that the HTML Document uses HTML5
<html lang="en">                                  // Declaring the HTML language helps the browser render it appropriately
  <head>
    <meta charset="UTF-8">                        // Declare the character set
    <title>HTML 5 Boilerplate Starter</title>     // Title of the page goes in the head
  </head>

  <body>
                    // The actual page content of the web page goes in the body
  </body>
</html>
```
<br>

## Head
The ```<head>``` of an HTML file is where various metadata is set. This is important information that helps the web browser properly parse and render the web page.  

The ```<head>``` is where Javascript files and CSS stylesheets will be linked to the HTML document. It is also where the ```<title>``` of the page is set and where the charset type is enforced (usually UTF-8 for English)

In the event that you are writing inline (in-document) CSS, the ```<head>``` is also where the ```<style>``` tags and your inline CSS would go.  
But **please do not write inline CSS as it is bad practice, use External Stylesheets**.

<br>

## Body
The ```<body>``` of an HTML file is the content that appears to someone viewing that page in a web browser. This is the only part of a web page that is easily Human-Readable and accessible to the layperson using the web. 

Any and all content meant to be viewed by the average internet user always goes in the ```<body>```.


<br>

### Headings
Headings in HTML help to organize information into categories and sub-categories of increasing complexity and information. 

```<h1>``` is the most important, and ```<h6>``` is the least important.

It is important to use headings correctly in web development, as screen readers rely on the correct use of headings to accurately parse pages for sight-impaired people.   
If a heading is too large, use CSS to resize it over using a less important heading. 

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```
<img src="../images/Headings.JPG">



### Example Web Page

Here is an example of a web page's HTML that you might see in real life: 

```html
<!DOCTYPE html>                                   
<html lang="en">                                 
  <head>
    <meta charset="UTF-8"> 
    <link rel="stylesheet" src="../style.css">                       
    <title>HTML 5 Boilerplate Starter</title>     
  </head>

  <body>
    <div>
      <span>Some Text</span>
    </div>     
  </body>
</html>
```
