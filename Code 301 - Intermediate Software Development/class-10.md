# In memory storage

## Understanding the JavaScript Call Stack

<https://medium.freecodecamp.org/understanding-the-javascript-call-stack-861e41ae61d4>

**What is a ‘call’?**

The call stack is primarily used for function invocation (call). 

**How many ‘calls’ can happen at once?**

1

**What does LIFO mean?**

LIFO: When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

**Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.**

function firstFunction(){
  console.log("Hello from firstFunction");
}

function secondFunction(){
  firstFunction();
  console.log("The end from secondFunction");
}

secondFunction();

<https://cdn-media-1.freecodecamp.org/images/oEp65Ec9CD4CnL7t0uSPoyzrkA1i1BR-Ij1n>

**What causes a Stack Overflow?**

A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

## JavaScript error messages

<https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c>

**What is a ‘reference error’?**

This is as simple as when you try to use a variable that is not yet declared you get this type os errors.

This is also a common thing when using const and let, they are hoisted like var and function but there is a time between the hoisting and being declared so when you try to access them a reference error occurs, the fact that this happens to let and const is called Temporal Dead Zone (TDZ).

Whatever you are using (var, let or const) the fix is as simple has declaring the variable before any declaration is made.

**What is a ‘syntax error’?**

 know it’s in the name of the errors, but like it says itself, this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

 JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1

 fix:

 JSON.parse('{"foo":"bar"}')

**What is a ‘range error’?**

Manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

var foo= []
foo.length = foo.length -1 // Uncaught RangeError: Invalid array length

**What is a ‘tyep error’?**

Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

var foo = {}
foo.bar // undefined
foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined

The most frequent error in JS, trying to access a property/method thinking that bar is of the type object when in reality, since it hasn’t been declared yet, it’s undefined which doesn’t have any baz available.

**What is a breakpoint?**

The breakpoint can also be achieved by putting a debugger statement in your code in the line you want to break.

You can also add conditional breakpoints by right-clicking a previous set breakpoint, which will make your program stop at that point only if a condition is met, this is awesome for when you want to debug huge cycles for specific values.

**What does the word ‘debugger’ do in your code?**

To debug your JS code, the easiest and maybe the most common way its to simply console.log() the variables you want to check or, by using chrome developer tools, open your page with your JS code (press cmd+o in macOS or Ctrl+o in Windows) and choose your file to debug, click the line you wanna debug and refresh your page again (F5).

If the line you selected was run you will be able to see what has happened before that point and you can try and evaluate the next lines to check if everything is outputting what you are expecting.

### Bookmark and Review

JavaScript errors reference on MDN <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors>

### Things I want to know more about

How to incorporate debugging effectively in my code.

quokka to evaluate your code as you type.