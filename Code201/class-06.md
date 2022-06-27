# JavaScript Object Basics

## How would you describe an object to a non-technical friend you grew up with?

An object is a collection of related data and/or functionality. These usually consist of several variables and functions (which are called properties and methods when they are inside objects).
const person = {};

[object Object]
Object { }
{ }

const person = {
  name: ['Bob', 'Smith'],
  age: 32,
  bio: function() {
    console.log(`${this.name[0]} ${this.name[1]} is ${this.age} years old.`);
  },
  introduceSelf: function() {
    console.log(`Hi! I'm ${this.name[0]}.`);
  }
};

person.name
person.name[0]
person.age
person.bio()
person.introduceSelf()

The first two items are data items, and are referred to as the object's properties. The last two items are functions that allow the object to do something with that data, and are referred to as the object's methods.





## What are some advantages to creating object literals?

Dot notation 
The object name (person) acts as the namespace — it must be entered first to access anything inside the object. Next you write a dot, then the item you want to access — this can be the name of a simple property, an item of an array property, or a call to one of the object's methods, for example:

person.age
person.bio()

Bracket notation
This looks very similar to how you access the items in an array, and it is basically the same thing — instead of using an index number to select an item, you are using the name associated with each member's value. It is no wonder that objects are sometimes called associative arrays — they map strings to values in the same way that arrays map numbers to values.


person['age']
person['name']['first']


How do objects differ from arrays?

Sending a single object is much more efficient than sending several items individually, and it is easier to work with than an array, when you want to identify individual items by name.


Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.

One useful aspect of bracket notation is that it can be used to set not only member values dynamically, but member names too. Let's say we wanted users to be able to store custom value types in their people data, by typing the member name and value into two text inputs.

Evaluate the code below. What does the term this refer to and what is the advantage to using this?
const dog = {
  name: 'Spot',
  age: 2,
  color: 'white with black spots',
  humanAge: function (){
    console.log(`${this.name} is ${this.age*7} in human years`);
  }
}

This keyword refers to the current object the code is being written inside.
This enables you to use the same method definition for every object you create.
In the above example this is referring to the this.name as Spot, this.age as 2.

# Introduction To The DOM

What is the DOM?

The Document Object Model (DOM) is the data representation of the objects that comprise the structure and content of a document on the web. This guide will introduce the DOM, look at how the DOM represents an HTML document in memory and how to use APIs to create web content and applications.

 (DOM) is a programming interface for web documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects; that way, programming languages can interact with the page


Briefly describe the relationship between the DOM and JavaScript.
https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction#fundamental_data_types

The Document Object Model (DOM) representation allows it to be manipulated. As an object-oriented representation of the web page, it can be modified with a scripting language such as JavaScript.

const paragraphs = document.querySelectorAll("p");
// paragraphs[0] is the first <p> element
// paragraphs[1] is the second <p> element, etc.
alert(paragraphs[0].nodeName);


Example is written in JavaScript, but uses the DOM to access the document and its elements. The DOM is not a programming language, but without it, the JavaScript language wouldn't have any model or notion of web pages, HTML documents, SVG documents, and their component parts. The document as a whole, the head, tables within the document, table headers, text within the table cells, and all other elements in a document are parts of the document object model for that document. They can all be accessed and manipulated using the DOM and a scripting language like JavaScript.

## Bookmark and Review

Understanding the problem domain is the hardest part of programming

http://simpleprogrammer.com/2013/07/15/understanding-the-problem-domain-is-the-hardest-part-of-programming

What’s the difference between primitive values and object references in JavaScript?

https://betterprogramming.pub/intermediate-javascript-whats-the-difference-between-primitive-values-and-object-references-e863d70677b

Classifying JavaScript’s Eight Data Types

JavaScript currently supports eight different data types. This includes seven primitive value types and objects.

Boolean
Null
Undefined
Number
BigInt
String
Symbol
Objects

Arrays, functions, and dates all play an important role in JavaScript programs, but they are really just objects under the hood.

The Difference Between a Value and a Reference

Primitive values and object references are stored in JavaScript programs in different ways.

When a primitive value is assigned to a variable (eg let foo = ‘bar’), the variable is set to that value directly.

When the variable is assigned with an object, however, things are different. Instead of containing the value directly, that variable contains a reference to it. Here’s an example:

const moe = {
  name: 'Moe Szyslak',
  occupation: 'Bartender',
  voicedBy: 'Hank Azaria'
}

When the code above is executed, JavaScript creates the object and stores it somewhere in computer memory. The variable moe does not contain the new object directly, it contains a reference to the memory address that currently stores the object.

One key difference between primitive values and object references is mutability. Primitive values are immutable and object references are mutable.

Put simply, this means that primitive values cannot be changed (or mutated), but object references can be changed.

## Things I want to know more about


