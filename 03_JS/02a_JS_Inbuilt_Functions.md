# Inbuilt Functions / Operators in Javascript
You may have noticed that strings have inbuilt functions, or operators, in javascript  
String operators like ```.indexOf``` are a good example of this

Many inbuilt functions are specific to the type of data being manipulated, such as string operators like ```trim```, or [Array Methods](../03_JS/10_Array_Methods.md), which we'll learn about later

But some inbuilt functions, like the ones in this document, are general to Javascript and are not tied to specific data types

<br> 

## ```typeof```
The ```typeof``` operator evauates the type of data it is being given and returns a string representing the type:

```js
var goodBoy = "dog"
var isCatBetter = true
var howManyCats = 11 

var catsCatsCats = function catCeption() {
                     if (howManyCats < 20) {
                      howManyCats++
                     }
                     return howManyCats
                   }
```

```js
var typeGoodBoy = typeof goodBoy 
console.log(typeGoodBoy);                           // "string"

var typeIsCatBetter = typeof isCatBetter
console.log(typeIsCatBetter);                       // "boolean"

var typeHowManyCats = typeof howManyCats  
console.log(typeHowManyCats);                       // "number"

var typeCatsCatsCats = typeof catsCatsCats
console.log(typeCatsCatsCats);                      // "function"
```

