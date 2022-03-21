# Inbuilt Functions / Operators in Javascript
You may have noticed that strings have inbuilt functions, or operators, in javascript  
String operators like ```.indexOf``` are a good example of this

Many inbuilt functions are specific to the type of data being manipulated, such as string operators like ```trim```, or [Array Methods](../03_JS/10_Array_Methods.md), which we'll learn about later

But some inbuilt functions, like the ones in this document, are general to Javascript and are not tied to specific data types

<br> 

## ```typeof```
The ```typeof``` function evauates the type of data it is being given and returns a string representing the type:

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
console.log(typeGoodBoy);                           // string

var typeIsCatBetter = typeof isCatBetter
console.log(typeIsCatBetter);                       // boolean

var typeHowManyCats = typeof howManyCats  
console.log(typeHowManyCats);                       // number

var typeCatsCatsCats = typeof catsCatsCats
console.log(typeCatsCatsCats);                      // function
```

<br>

## ```Number();```
The ```Number();``` function intakes a string and transforms it into a number type  
This is very useful if you have some sort of user input or incoming data that has numerical characters as strings instead of numbers and you need to perform mathematical operations on those strings. 

**What happens when you try to add a string and an number? Concatenation!**
```js
var firstNumber = 100
var secondNumber = "2"


var added = firstNumber + secondNumber;
console.log(added);                                 // 1002
console.log(typeof added);                          // string
```
What happened? Why is this not ```102```?

```"2"``` is a string, not a number like ```100``` -- so ```100``` and ```"2"``` became the concatenated string ```"1002"```

**Now, the magic of ```Number();```:**
```js
var firstNumber = 100
var secondNumber = "2"

var added = firstNumber + Number(secondNumber);
console.log(added);                                 // 102
console.log(typeof added);                          // number
```
<br>

Keep in mind that this only works if the string in question cabe evaluated as a number:
```js
var addMore = 10 + Number("9a")
console.log(addMore);                               // NaN
```
Here, the result is ```NaN```, or Not a Number