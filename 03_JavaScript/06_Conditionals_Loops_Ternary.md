# Conditionals, Loops, and Ternary Statements

## Conditionals
### If Statements
```js
function isItTrue(){
  if (true === true) {                // ? If true strict-equals (===) true,
      console.log("true");            // ? print true
  }
}
```

<br>

### Else Statements
```js
function isItACat(){
  let c = "cat"                       // ? let c represent cat

  if ( c === "dog") {                 // ? if c strict-equals "dog",
    console.log("I'm a dog!");        // ? print "I'm a dog!"
  } else if (c === "turtle") {        // ? or if not, try if c strict-equals "turtle"
    console.log("I'm a turtle!");     // ? and print "I'm a turtle!"
  } else if (c === "aardvark") {      // ? or if not try if c strict-equals "aardvark"
    console.log("I'm an aardvark!");  // ? print "I'm an aardvark!"
  } else {                            // ? or, if NONE of those worked, default to:
    console.log("it's a mystery!");   // ? print "it's a mystery!"
}
```

<br>

## Loops
For and While loops allow code to be executed indefinitely as long as a condition is met

For loops are great when you know how many iterations you need (e.g. as many as it takes to get through a list)

While-loops are great when you have no idea when the iterations will need to stop \ when you want a specific condition to happen and the loop shouldn't stop until then (e.g. until the user finally enters valid input [input validation!] -- or until the user decides to close a menu, etc)

### While Loop
```js
function countUpWhile(){

let index = 0                          // set the variable for the condition being met and give it a value

// ! notice that the index variable is initialized /outside/ the while loop


while (index < 5) {                    // while the variable index is less than 5
  console.log("counting up...")        // print counting up...
  index ++                             // and increment variable index by 1
}
};

countUpWhile();
// this is a classic while loop
// this code will print counting up... 5x before quitting
```

<br>

### For Loop
```js
function countUpFor(){

for (index = 0; index < 5 ; index ++){  // the same logic as while on one line. Set the variable for the condition 
                                        // being met and give it a value. While the variable index is less than 5,
                                        // increment variable index by 1

            // ! notice that the index variable is initialized /inside/ the for loop

  console.log("counting up...")         // and print counting up...
}
};

countUpFor();
// this is a classic for loop
```

<br>

## ```break``` statement


<br>

## Ternary Statements
Let's set up an object and a couple variables:
```js
var friend1= {firstName:"Alex", lastName:"Smith", age: 21}

var myFriend;
var isOfAge;
```
Take this if statement: 
```js
if (friend1.age >= 21){
  isOfAge = true;
}
else {
  isOfAge = false;
}
```

Five lines of code

How can we make that shorter? **Ternary Statements!**
Ternary Statement structure is:
```
variable = expression ? valueForTrue : valueForFalse
```
```js
isOfAge = friend1.age >= 21 ? true : false;
```
This says basically the same thing as the ```if``` statement above, but in one line

**HOWEVER**, it is important to remember that writing [Human-Readable Code](../00_START_HERE/03_Human_Readable_Code.md) is more important than writing code that takes less lines. 
