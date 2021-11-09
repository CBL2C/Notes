# Strings, Indexing, Interpolation
## Strings
What are Strings?
  - strings represent literal text
  - a string is a sequence of characters surrounded by quotation marks " " or ' '
  - strings are technically [arrays](../03_JS/09_Arrays.md) of characters arranged in a human-meaningful way: this is why strings can be [indexed](#indexing)

```js
Examples:
'potato';
"New York";
"amanda@gmail.com";
"Follow the yellow brick road, please!";
"365 days a year";
"";
" ";
"... ";
```

### Escape characters with backslash \
```js
"He said, \"what's up?\"";
```
- here, "What's up?" is counted as a string WITH the double quotes. Using \ allows the double quotes (or any symbol escaped) to become a character in a string


### Why use different quotes?
```js
'Shakespeare wrote, "To be or not to be"';
// for putting quotes or dialouge in strings
"That's a great string";
// for putting apostrephes in strings
```
Strings must have their opening and closing quotes match
Strings must not have the same quotes inside them as punctuation:
```js 
'That's a bad string';
```

<br>

### Counting String Length
**```.length``` will give you the number of characters in a string:**
```js
let ramen = "ramen"
console.log("ramen".length);        // 5
console.log("go home!".length);     // 8
// the spacebar counts as a placeholder and adds towards total length
console.log("".length);             // 0
// an empty string returns 0 for length
```

<br>


## Concatenating Strings and ```.concat```
Concatenation is joining two strings together
```js
console.log("hello" + "world");             // 'helloworld'
console.log("goodbye" + " " + "moon");      // 'goodbye moon'

let str1 = "hello_"
let str2 = "world"
console.log(str1 + str2);                   // 'hello_world'
```

In addition to using the ```+``` operator, strings can also be concatenated with ```.concat```:
```js
let strA = "Bippity Boppity"
let strB = "Boo"
console.log(strA.concat(" ", strB));             // 'Bippity Boppity Boo'
```

<br>

## ```.trim()```
An inbuilt string function, ```.trim()``` trims the whitespace from a string variable and returns a **new string**
```js
let message = " What a beautiful day! "
console.log(message);                       // " What a beautiful day! "
message.trim();                             // "What a beautiful day!"
```
<br>

## Indexing
Indexes start at 0
The index will always be 1 less than the ```.length```
```js
console.log("cat".length);          // 3
console.log("cat"[3]);              // undefined
console.log("cat"[0]);              // 'c'
console.log("cat"[2]);              // 't'

// Examples:
console.log("marigold"[0]);         // 'm'
console.log("marigold"[1]);         // 'a'
console.log("marigold"[2]);         // 'r'
console.log("marigold"[3]);         // 'i'
console.log("marigold"[7]);         // 'd'
console.log("marigold"[10]);        // undefined
console.log("marigold"[-3]);        // undefined
//  if an index number is out of scope (-3, 41 for cat, etc) the REPL returns undefined
```

<br>

### Fun with ```.length``` and ```.indexOf```
```js
console.log("h4xx0r"["h4xx0r".length])
```
here, you are asking for js to find the length of the string "haxxor" as an index -- but because the index is always one less than the string length, it returns undefined

```js
console.log("h4xx0r"["h4xx0r".length - 1])
```

here, this will always find the last letter of the string (because the index is always one less than the character count / length)

<br>

### Finding the Indexed Letter
```.indexOf``` starts at a beginning of a string checking for characters
once it finds the character it's looking for it returns and stops executing
```js
console.log("bagel".indexOf("b"));  // 0
console.log("bagel".indexOf("a"));  // 1
console.log("bagel".indexOf("l"));  // 4
console.log("bagel".indexOf("z"));  // -1
// ! if the letter does not exist, -1 will return

// ? what if the letter appears more than once?
console.log("baaaa".indexOf("a"));  // 1
// the indexOf retured will be the first occurrence
```

<br>

### Finding the Indexed Character Snippet
```.indexOf``` will return the inxex at the START of the snippet
```js
console.log("door hinge".indexOf("oor"));   // 1
console.log("door hinge".indexOf("hi"));    // 5
console.log("door hinge".indexOf("hint"));  // -1
// if the snippet does not exist, -1 will return
```

<br>


## String Interpolation
**Ever seen ```${ }``` in javascript?**

```js
let firstName = 'Doctor'
let lastName = 'Who'

// ! anything inside `${ } ` will be interpreted as javascript
let sentence = `hello ${firstName} ${lastName}`
      // hello Doctor Who

// | Basic expressions work as well
let sentence2 = `${2+1} is larger than ${2-1}`
      // 3 is larger than 1
```