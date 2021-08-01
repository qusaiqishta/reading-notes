# ES6 Syntax and Feature Overview

## Arrow functions
The arrow function expression syntax is a shorter way of creating a function expression. Arrow functions do not have their own this, do not have prototypes, cannot be used for constructors, and should not be used as object methods.

ES5
```
function func(a, b, c) {} // function declaration
var func = function (a, b, c) {} // function expression
```
ES6
```
let func = (a) => {} // parentheses optional with one parameter
let func = (a, b, c) => {} // parentheses required with multiple parameters
```

## Template literals

- concatination:
```
var str = 'Release date: ' + date
```

- interpolation

```
let str = `Release Date: ${date}`
```

## Implicit returns
The return keyword is implied and can be omitted if using arrow functions without a block body.

```
function func(a, b, c) {
  return a + b + c
}

```
```
let func = (a, b, c) => a + b + c // curly brackets must be omitted
```
## Method definition shorthand
The function keyword can be omitted when assigning methods on an object.

```
var obj = {
  a: function (c, d) {},
  b: function (e, f) {},
}
```

```

let obj = {
  a(c, d) {},
  b(e, f) {},
}
```

## Array iteration (looping)
A more concise syntax has been introduced for iteration through arrays and other iterable objects.

```
var arr = ['a', 'b', 'c']

for (var i = 0; i < arr.length; i++) {
  console.log(arr[i])
}

for (let i of arr) {
  console.log(i)
}
```

## Spread syntax
Spread syntax can be used to expand an array.

```
let arr1 = [1, 2, 3]
let arr2 = ['a', 'b', 'c']
let arr3 = [...arr1, ...arr2]

console.log(arr3) // [1, 2, 3, "a", "b", "c"]
```

## Classes/constructor functions
ES6 introducess the class syntax on top of the prototype-based constructor function.

```
function Func(a, b) {
  this.a = a
  this.b = b
}

Func.prototype.getSum = function () {
  return this.a + this.b
}

var x = new Func(3, 4)
```


```

class Func {
  constructor(a, b) {
    this.a = a
    this.b = b
  }

  getSum() {
    return this.a + this.b
  }
}

let x = new Func(3, 4)

x.getSum() 
```

## Inheritance
The extends keyword creates a subclass.

```
function Inheritance(a, b, c) {
  Func.call(this, a, b)

  this.c = c
}

Inheritance.prototype = Object.create(Func.prototype)
Inheritance.prototype.getProduct = function () {
  return this.a * this.b * this.c
}

var y = new Inheritance(3, 4, 5)
```

```  
function Inheritance(a, b, c) {
  Func.call(this, a, b)

  this.c = c
}

Inheritance.prototype = Object.create(Func.prototype)
Inheritance.prototype.getProduct = function () {
  return this.a * this.b * this.c
}

var y = new Inheritance(3, 4, 5)

y.getProduct()
```

## Modules - export/import
Modules can be created to export and import code between files.

```
<script src="export.js"></script>
<script type="module" src="import.js"></script>
```

```
let func = (a) => a + a
let obj = {}
let x = 0

export {func, obj, x}
```

```
import {func, obj, x} from './export.js'

console.log(func(3), obj, x)
```

## Promises/Callbacks
Promises represent the completion of an asynchronous function. They can be used as an alternative to chaining functions.


```
function doSecond() {
  console.log('Do second.')
}

function doFirst(callback) {
  setTimeout(function () {
    console.log('Do first.')

    callback()
  }, 500)
}

doFirst(doSecond)
```

```
let doSecond = () => {
  console.log('Do second.')
}

let doFirst = new Promise((resolve, reject) => {
  setTimeout(() => {
    console.log('Do first.')

    resolve()
  }, 500)
})

doFirst.then(doSecond)
```

# React Js


React. js is an open-source JavaScript library that is used for building user interfaces specifically for single-page applications. It's used for handling the view layer for web and mobile apps. React also allows us to create reusable UI components.


A samll react js example that  displays a heading saying “Hello, world!” on the page. will be like :

```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

## Rendering an Element into the DOM

Let’s say there is a <div> somewhere in your HTML file:
```
<div id="root"></div>
```

To render 'hello world inside the div :

```
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```

## Updating the Rendered Element
React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.

With our knowledge so far, the only way to update the UI is to create a new element, and pass it to ReactDOM.render().

Consider this ticking clock example:

```
function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  ReactDOM.render(element, document.getElementById('root'));
}

setInterval(tick, 1000);
```

### React Only Updates What’s Necessary
React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.
for example, in the previous example , react will only update h2 tag the contains the changing time 


## JSX
```
const element = <h1>Hello, world!</h1>;
```
This funny tag syntax is neither a string nor HTML.

It is called JSX, and it is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.

## Why JSX 
JSX allows us to write HTML elements in JavaScript and place them in the DOM without any createElement() and/or appendChild() methods. JSX converts HTML tags into react elements. You are not required to use JSX, but JSX makes it easier to write React applications.


## Embedding Expressions in JSX

In the example below, we declare a variable called name and then use it inside JSX by wrapping it in curly braces:

```
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;

ReactDOM.render(
  element,
  document.getElementById('root')
);
```


In the example below, we embed the result of calling a JavaScript function, formatName(user), into an <h1> element.

```
function formatName(user) {
  return user.firstName + ' ' + user.lastName;
}

const user = {
  firstName: 'Harper',
  lastName: 'Perez'
};

const element = (
  <h1>
    Hello, {formatName(user)}!
  </h1>
);

ReactDOM.render(
  element,
  document.getElementById('root')
);
```

## JSX is an Expression Too
After compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.

This means that you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions:
```
function getGreeting(user) {
  if (user) {
    return <h1>Hello, {formatName(user)}!</h1>;
  }
  return <h1>Hello, Stranger.</h1>;
}
```

## JSX Prevents Injection Attacks
It is safe to embed user input in JSX:
```
const title = response.potentiallyMaliciousInput;
// This is safe:
const element = <h1>{title}</h1>;
```
By default, React DOM escapes any values embedded in JSX before rendering them. Thus it ensures that you can never inject anything that’s not explicitly written in your application. Everything is converted to a string before being rendered. This helps prevent XSS (cross-site-scripting) attacks.

# Tailwind CSS
 is self-described as a utility first CSS framework. Rather than focusing on the functionality of the item being styled, Tailwind is centered around how it should be displayed. This makes it easier for the developer to test out new styles and change the layout.
