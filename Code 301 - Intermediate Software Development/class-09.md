# Functional Programming

## Functional Programming Concepts

<https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa>

**What is functional programming?**

Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data — Wikipedia

**What is a pure function and how do we know if something is a pure function?**

It returns the same result if given the same arguments (it is also referred as deterministic)

It does not cause any observable side effects

**What are the benefits of a pure function?**

There is no external object so we will always have the same result.

Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result.

**What is immutability?**

Unchanging over time or unable to be changed.

When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

**What is Referential transparency?**

Basically, if a function consistently yields the same result for the same input, it is referentially transparent.

pure functions + immutable data = referential transparency

## Videos

<https://www.youtube.com/watch?v=xHLd36QoS4k>

**What is a module?**

A module is JavaScript code split into different files by thier functionality.

**What does the word ‘require’ do?**

It tells the program that the module functionality in another file is required within the file you are working in.

**How do we bring another module into the file the we are working in?**

Require it in the current file like 

var counter = require('./counter');

**What do we have to do to make a module available?**

Set it as an module.export.functionName = functionName
