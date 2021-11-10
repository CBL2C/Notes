# Functions
Functions are pieces of code written once and called as many times as needed.

Functions require:
- The name of the function (unless it is an anonymous function)
- Parentheses ```()```, which tell javascript that this is a function to run
- An optional list of parameters for the function, enclosed in the parentheses ``()``
- The code to execute when the function runs, enclosed in curly braces ```{}```

```js
addNumbers() {
  let sum = 5
  sum += 6
  console.log(sum)      // 11
}
```
<br>

## First Class Objects
- Functions are First Class Objects in JavaScript
- First Class objects can be:
    - Stored in a [variable](../03_JS/01_JS_Basics.md), [Object](../03_JS/12_Objects_Nested_Destructuring.md), or [Array](../03_JS/09_Arrays.md)
    - Passed as an argument to a function
    - returned from a function

<br>

## Function Definition
```js
function myFunction(parameter1,parameter2){   // ? (the parameter(s) of the function)
    // ? some code to execute goes here
  }

// # Calling a Function
myFunction(argument1,argument2)           // ? the arguments passed to the function
```

<br>

### Parameters
**The following function does not use real numbers.**  
**Instead, it uses parameters.** 
```js
function average(number1, number2) {
  // On line 158 these arguments are "10,16"
    return (number1 + number2) / 2;           // ? add two arguments together, divide sum by 2
  }

  // This function call passes the arguments 10 and 16.
  average(10, 16)                             // 13
```

when defining a function with parameters, you are declaring those parameters as usable variables within that function.  
```number1``` and ```number2``` are now *parameters*, or variables specifically passed to the function

<br>

**Sometimes functions do not have included parameters**
```js
function testMe(){
  // some code to execute
}

// here are two examples of a function, one without parameters and one with:
function callMe() {
  console.log("Second!");        // "Second!"
  console.log("Third!");         // "Third!"
}
callMe();

function callMe(catchyWord) {
  console.log(catchyWord);
    }

callMe("Maybe?");                // Maybe?
```
In this example above, when we invoke ```callMe();``` we are *passing* ```"second"```, ```"third"``` and ```"catchyWord"``` *into the function* ```callMe();```-- each of these strings being passed in is called an *argument*
<br>

#### Arguments
When you invoke a function with parameters, you *must* pass in **arguments** for those parameters:
```js
function callMe(catchyWord) {
  console.log(catchyWord);
    }

callMe();                        // throws error
```
```js
function callMe(catchyWord) {
  console.log(catchyWord);
    }

callMe("Maybe?");                // Maybe?
```

**Arguments are positional.** 

They do not rely on anything except their position in the function invocation, and that position's relation to the parameters in the function being called:
```js
function addThreeNums(first, second, third){
  console.log(first + second + third)
}

addThreeNums(1, 2, 3);
```
Here, ```first``` is ```1```, ```second``` is ```2```, and ```third``` is ```3```  

<br>

### ```return``` and functions
```js
// functions return "undefined" by default
function addTwo(num1, num2){
  num1 + num2;
}

console.log(addTwo(1,2));        // undefined
```
This function did not run correctly

**What happened?**
The function needs to return the value
Right now if you dropped a debugger below num1 + num2, it would be evident that num1 + num2 is working correctly and evaluating as an expression. 
However, without telling JS to return the value or assign it to a variable, this function **WILL NOT** save the value of this equation.

**Let's fix that:**
```js
function addTwo(num1, num2){
  return num1 + num2;

}
console.log(addTwo(1,2));        // 3
```


**When using return, keep in mind that nothing PAST return will execute**
```js
function addTwo(num1, num2){
  return num1 + num2;            // ? return the value
}

console.log(addTwo(1,2));        // 3
```

**Returning the value makes the function stop after that line**
```js
function addTwo(num1, num2){
  return num1 + num2;            // ? return the value
  // ! NOTHING will run after this line!
  // ! ANY code after this line simply acts like it does not exist!
}

console.log(addTwo(1,2));        // 3
```

<br>


## Function Expression Syntax
Functions can be declared using Function Declaration or Function Expression Syntax

Function Declaration is already familiar:

### Function Declaration
```js
function newFunction(parameter1,parameter2){
    // some-code
}
```

Function expression looks a bit different: 
### Function Expression
```js
let newFunction = function (parameter1,parameter2){
    // some-code
}
```
