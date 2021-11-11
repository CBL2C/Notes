# Human-Readable Code

**In any journey to becoming a developer, it is important to remeber this adage:**
```
Beginner and Junior developers write longer, human-readable, easy code

Intermediate hotshot developers write one-line, slick, less readable code that looks impressive

Advanced Senior developers write longer, human-readable, easy code, with occasional slick tricks in logical places
```
**What is Human-Readable Code?**  
Human-readable code is just that: code that is easily readable and decipherable by another developer who did not have anything to do with that code's development
<br>

**Imagine this scenario:**  
You write a program, intending to develop it in the slickest, shortest, one-line code that you can. You do so. It is beautiful, a work of art. Difficult to read through line-by-line, but you're so proud of how short it is! 
Then, life happens. Your cat has kittens. Your boss's sister's best friend's uncle gets married. Months pass. You forget you ever wrote that program
One day, years later, you open an old folder and find it. You open it in your IDE of choice and... what on earth is this half-readable gibberish? 

Now imagine you are a new junior developer opening a file to work on at your new job. The code is clear, well-formatted, and has few shortcuts or one-liners. Even with your somewhat limited coding experience you can get through this file and make the changes your team needs. You get done with your work and feel good about your contribution to your job and your overall ability to code
<br> 

**Writing human-readable code is a critical skill of a good developer**  
Human-readable code may be code with longer lines, but it is overall easier to read, decipher, and maintain. 

<br>

(**The following example, from [This Extrenal Resource](https://dev.to/laurieontech/human-readable-javascript-337o), uses [arrow function syntax](../03_JS/05_Arrow_Functions.md) and the [array .map method](../03_JS/10_Array_Methods.md)** - however understanding either is not necessary for this material)

Consider this arrow function:
```js
const arr = [1,2,3]
let multipliedByTwo = arr.map(el => el*2)
```

Now, consider this version of that code:
```js
const arr = [1,2,3]
const timesTwo = (el) => el*2
let multipliedByTwo = arr.map(timesTwo)
```

Breaking the arrow function's original logic into three lines and passing ```.map``` the arrow function ```timesTwo``` significantly clarifies what it is this code is doing. By simply adding more explicit logic, this code becomes much more simple to read and understand by developers of all skill levels 