# ```this```
The ```this``` keyword is incredibly broad. It is **entirely contextual** in its usage, and ```this``` has both **global** and **function** ***contexts***.   

The behavior of ```this``` also changes between strict and non-strict modes.

## Using ```this```

### Global Context
In the global context, the this references the global object, which is the window object on the web browser or global object on Node.js.

This behavior is consistent whether the strict mode is applied or not, like this:

```js
console.log(this === window); // true
```
If you assign a property to this object in the global context, JavaScript will add the property to the global object as shown in the following example:

```js
this.color= 'Red';
console.log(window.color); // 'Red'
```