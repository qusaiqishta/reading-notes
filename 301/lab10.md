# Call stack

A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.

- When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function

- Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.

- When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.

- If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

```
function greeting() {
   // [1] Some code here
   sayHi();
   // [2] Some code here
}
function sayHi() {
   return "Hi!";
}

// Invoke the `greeting` function
greeting();

// [3] Some code here
```
The code above will be excuted like following 

1- Ignore all functions, until it reaches the greeting() function invocation.

2-Add the greeting() function to the call stack list
```
Call stack list:
- greeting
```

3-Execute all lines of code inside the greeting() function.

4-Get to the sayHi() function invocation.

5-Add the sayHi() function to the call stack list

```
Call stack list:
- sayHi
- greeting

```
6-Execute all lines of code inside the sayHi() function, until reaches its end.

7-Return execution to the line that invoked sayHi() and continue executing the rest of the greeting() function.

8-Delete the sayHi() function from our call stack list
```
Call stack list:
- greeting
```

9-When everything inside the greeting() function has been executed, return to its invoking line to continue executing the rest of the JS code.

10-Delete the greeting() function from the call stack list.


In summary, then, we start with an empty Call Stack. Whenever we invoke a function, it is automatically added to the Call Stack. Once the function has executed all of its code, it is automatically removed from the Call Stack. Ultimately, the Stack is empty again.


### In other word 
a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).

LIFO: When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

```

function firstFunction(){
  throw new Error('Stack Trace Error');
}

function secondFunction(){
  firstFunction();
}

function thirdFunction(){
  secondFunction();
}

thirdFunction();

```

You will notice that the arrangement of the functions as a stack begins with the firstFunction() (which is the last function that got into the stack, and is popped out to throw the error), followed by the secondFunction(), and then the thirdFunction() (which is the first function that gets pushed into the stack when the code is executed).


**Manage function invocation (call):** The call stack maintains a record of the position of each stack frame. It knows the next function to be executed (and will remove it after execution). This is what makes code execution in JavaScript synchronous.


## What causes a stack overflow?

A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

```
function callMyself(){
  callMyself();
}

callMyself();

```

# Error types:

- Reference errors

This is as simple as when you try to use a variable that is not yet declared you get this type os errors.
```
console.log(foo) // Uncaught ReferenceError: foo is not defined
```

- Syntax errors
this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.
```
JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1
```
it can be solve like this
```
JSON.parse('{"foo":"bar"}')
```
- Type errors

```
var foo = {}
foo.bar // undefined
foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined
```