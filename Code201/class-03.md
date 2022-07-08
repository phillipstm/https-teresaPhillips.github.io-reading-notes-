# HTML Lists, CSS Boxes, JS Control Flow

## Learn HTML
### Ordered and Unordered Lists

* Ordered List

numbered as a list in sequencial order for a list of procedures.

* Unordered List

a list of items in no particular order

### When should you use an unordered list in your HTML document?


When marking up content which could be defined in some way as a list, you should consider using an unordered list (<ul>) for presentation. Not only does it improve the readability of your HTML code, it also applies meaning to content which would otherwise have none.

### How do you change the bullet style of unordered list items?

Change bullet style for an unordered list. Just as you can change the numbering style for an ordered list, you can change the default bullet style for an unordered list with the type attribute. The three possible values for an ordered list include: disc - the default type, represented by a solid circle.

### When should you use an ordered list vs an unorder list in your HTML document?


You would want to use an <ol> if you need step by step instructions.
Steps in a recipe
Turn-by-turn directions
The list of ingredients in decreasing proportion on nutrition information label

The <ul> element is for grouping a collection of items that do not have a numerical ordering, and their order in the list is meaningless. Typically, unordered-list items are displayed with a bullet, which can be of several forms, like a dot, a circle, or a square. The bullet style is not defined in the HTML description of the page, but in its associated CSS, using the list-style-type property.

### Describe two ways you can change the numbers on list items provided by an ordered list?

Double-click the numbers in the list. The text won't appear selected.
Right-click the number you want to change.

Click Set Numbering Value.
In the Set value to: box, use the arrows to change the value to the number you want.


## Learn CSS
### The Box Model

### Describe the CSS properties of margin and padding as characters in a story. What is their role in a story titled: “The Box Model”?

The CSS margin properties are used to create space around elements, outside of any defined borders.

The CSS padding properties are used to generate space around an element's content, inside of any defined borders.

### List and describe the four parts of an HTML elements box as referred to by the box model.

The four components are Content, Padding, Border and Margin. HTML


## Learn JS
### Arrays, Operators and Expressions. Conditionals and Loops.


### What data types can you store inside of an Array?

Arrays. Operators and Expressions. Conditionals. Loops.


### Is the people array a valid JavaScript array? If so, how can I access the values stored? If not, why?


const people = [['pete', 32, 'librarian', null], ['Smith', 40, 'accountant', 'fishing:hiking:rock_climbing'], ['bill', null, 'artist', null]];

No, It looks like a chaining assignment.


### List five shorthand operators for assignment in javascript and describe what they do.

Comparison operators

Arithmetic operators

Bitwise operators

Bitwise logical operators

Bitwise shift operators



### Read the code below and evaluate the last expression and explain what the result would be and why.
 let a = 10;
 let b = 'dog';
 let c = false;

 // evaluate this
 (a + c) + b;

An expression is any valid unit of code that resolves to a value.

### Describe a real world example of when a conditional statement should be used in a JavaScript program.

Conditional statements control behavior in JavaScript and determine whether or not pieces of code can run.

### Give an example of when a Loop is useful in JavaScript.

JavaScript loops provide a quick and easy method of doing something repeatedly without redoing the code.

### Bookmarks


https://cssgridgarden.com/

#garden {
  display: grid;
  grid-template-columns: 20% 20% 20% 20% 20%;
  grid-template-rows: 20% 20% 20% 20% 20%;
}

#poison {
grid-column-start: 5;
}