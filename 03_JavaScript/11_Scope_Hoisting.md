# Scope and Hoisting

## Scope 
The scope of a function in JS is the set of variables that are accessible at a given location in that function

Scope is very important and, at times, feels very abstract. Because of this do not try to fully understand Scope right away nor how you would apply it in the future.

Instead, try to understand how it is currently blocking you form a particular task. Once your build up your software development skills and start writing more abstract code, you will naturally find yourself in new scenarios that require that next level of understanding.


### Types of Scope in JS
**Global** - Variables defined in the global scope.

**Local or Function** - Global, Parameters, Variables in the function

**Block** - Global, Local, Variables in the block

<br>

### Global Scope:
Variables declared ouside any function, just out in the open, are considered globally scoped
```js
    const bear = {
        sound: "RAWR!" 
        }
```


***Global*** Scope in javascript can also refer to a web browser window, if the javascript is being deployed in a web environment. In this case, anything globally scoped with have access to the entire browser window. 

<br>

### Local (Function) Scope:
Variables declared inside of a function are 'locally-scoped' - they **cannot** be referenced outside of the function
```js
    function bearMaker(name){
        let bearString = "I'm " + name + " the bear Rawr!"
        return bearString
    }
    console.log(bearMaker("Miley"));
```
Here, the ```bearMaker();``` function has access to:
- incoming arguments (```name```)
- variables declared in the function (```bearString```)
- any previously declared variables in the Global Scope
<br>

### Block Scope:
```js
    if (true) {
        let candle = "fire!"
        console.log(fire);
    }
```

<br>

### Scope Chaining:
When a function is given a variable it does not have declared in its scope, it will attempt to find a variable within the scope, then go up one scope level to find the variable

```js
    function garden() {
        let flower = "lily"

        function flowerBed(){
            console.log(flower)
        }
        flowerBed();
    }
    garden();                            // "lily"
```

A function will always use the scope closest to it first. Variable scope works inside ---> to out, but not outside to in
```js
    function garden() {
        let flower = "lily"

        function flowerBed(){
            let flower = "Not a lily"    // closest scope for flowerBed
            console.log(flower)
        }
        flowerBed();
    }
    garden();                            // "Not a lily"
```

<br>

## Variable Types
### Const, Let, and Var

### ```let```
Functions with let
```js
let hungry = false

    function sayHungry() {
        let hungry 
        hungry = true

        if (hungry) {
            let hungry = potato
            console.log(hungry);        // potato
        }
        console.log(hungry);            // true
    }
    console.log(hungry);                // false
```

### ```var```
#### Functions with ```var```
**(Don't Use ```var``` unless you are willing to put up with ```var```'s behavior)**

```var``` is Function-scoped or Globally-Scoped and does not behave like ```let``` or ```const``` 
```js
var hungry = false

    function sayHungry() {
        var hungry 
        hungry = true

        if (hungry) {
            var hungry = potato
            console.log(hungry);        // potato
        }
        console.log(hungry);            // potato
    }
    console.log(hungry);                // false
```

### const 
#### Functions with const
- const CANNOT be redefined -- it stands for 'constant'
- const is block-scoped
- const CAN be reinitialized (a variable of the same name can be initialized) by using const again in a different block
```js
const hungry = false

    function sayHungry() {
        const hungry 
        hungry = true

        if (hungry) {
            const hungry = potato
            console.log(hungry);        // potato
        }
        console.log(hungry);            // true
    }
    console.log(hungry);                // false
```
---

## Hoisting
### var
```js
    function hoist(){
        console.log(dog)
        var dog = 'Rosie'
        // var is "hoisted" -- variable dog can be called before it is declared
    }

    hoist();
```

- var is weird, don't use it
```js 
    return var
    var food = "egg"
    // here return var will return undefined 

    var food;
    return var;
    food = "egg"    
    // here due to hoisting var food can be initialized after being called
    // and it will still work because it was already declared 
```
### let 
```js
    function hoist(){
        console.log(dog)
        let dog = 'Rosie'                  
        // temporal dead zone -- variable dog cannot be used before declaring
    }

    hoist();
```

### const
```js
function hoist(){
    console.log(dog)
    const dog = 'Rosie'                  
    // temporal dead zone -- variable dog cannot be used before declaring
}

hoist();
```
---

## Closures
An inner function that uses (or changes) variables that were initialized in an outer function

```js
    // Example 1:
    function appleTree() {
        let aVariable = 'apple';

        function tree() {
            // the inner function has access to the outer function
            return aVariable;               
            // returns a `closed over` variable `aVariable`
        }

        return tree();
    }
    console.log(appleTree());             // "apple"
```
---
```js
    // Example 2:
    function appleTree2() {
        let tree = { type: 'apple', grown: false };
    
        function growTree() {
            tree.grown = true; 
            // changing a `closed over` variable `tree`
        }
    
        growTree();
        return tree;
    }
    console.log(appleTree2());
```
---
```js
    // Example 3:
    function treeMaker() {
        let trees = [];
    
        function addTree(tree) {
            trees.push(tree);
            return trees;
        }
    
        return addTree; 
        // remember, we are returning a function here
    }
    
    const treeFunc = treeMaker();
    console.log(treeFunc);
    console.log(treeFunc('Pine'));
```
---
```js
    // Example 4:
    function createCounter() {
        let count = 0;
    
        return function () {
            // we are returning an anonymous function here
            count++; 
            // we are changing a closed over variable here
            return count;
        };
    }
    let counter1 = createCounter();
    console.log(counter1);
    console.log(counter1());
    console.log(counter1());
    
    let counter2 = createCounter();
    console.log(counter2);
    console.log(counter2());
    console.log(counter2());
```
---
```js
    // Example 5: 
    function pizzaMaker(food) {
        // we are inside the `outer` function
        let order = "I'd like a pizza with ";
    
        function oven() {
            // we are inside the `inner` function
            return order + food; 
            // food comes from the outer scope (see line 265)
        }
    
        return oven();
    }
    
    console.log(pizzaMaker('cheese'));
```
---
```js
    // Example 6:
    function groceryList(list) {
        let groceries = list;                      // [ 'milk, 'eggs' ]
    
        function addItem() {
            groceries.push('and ice cream!');      // [ 'milk', 'eggs', 'and ice cream' ]
            // mutates closed over `groceries` variable
        }
    
        addItem();
        return groceries;                          // [ 'milk', 'eggs', 'and ice cream' ] 
    }
    console.log(groceryList(['milk', 'eggs']));
```
---
```js
   // Example 7:
   function elephantCollector() {
    const elephants = ['dumbo'];

    return function (name) {
        // we are returning a FUNCTION
        elephants.push(name);
        return elephants; 
        // this is a CLOSED OVER variable
    };
    }

    const elephantParade = elephantCollector();
        // returns a function
    console.log(elephantParade);
    console.log(elephantParade('Obi'));
    console.log(elephantParade('Gerald'));
```
---
