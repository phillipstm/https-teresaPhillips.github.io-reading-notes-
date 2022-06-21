

## Compose a short poem describing how HTTP sends data between computers.



## Describe how HTML, CSS, and JS files are “parsed” in the browser.

Parsing means analyzing and converting a program into an internal format that a runtime environment can actually run, for example the JavaScript engine inside browsers.

### HTML parsing
HTML parces data into a DOM * Document Object Model. HTML parsing involves tokenization and tree construction. HTML tokens include start and end tags, as well as attribute names and values.
### CSS parsing
It parses the text into the CSS Object Model (or CSSOM), a data structure it then uses for styling layouts and painting. The browser then creates a render tree from both these structures to be able to paint the content to the screen. JavaScript is also downloaded, parsed, and then executed.
### JS parsing
JavaScript parsing is done during compile time or whenever the parser is invoked, such as during a call to a method.


## How can you find images to add to a Website?

You can find images on Google images




## How do you create a String vs a Number in JavaScript?

Creating a String requires placing it in single quote marks '5' + '5'. This is a string of text.

Creating a number in JS you wouldn't place the numbers or data inside quotes. Example 5+5=10 it would give the expected result. 



## What is a Variable and why are they important in JavaScript?

Variables are containers that store data. You start by declaring the variable with *let* keyword followed by the name given to the variable.

Variable	Explanation 	Example
*String*	This is a sequence of text known as a string. To signify that the value is a string, enclose it in single quote marks.	let myVariable = 'Bob';

*Number*	This is a number. Numbers don't have quotes around them.	let myVariable = 10;

*Boolean*	This is a True/False value. The words true and false are special keywords that don't need quote marks.	let myVariable = true;

*Array*	    This is a structure that allows you to store multiple values in a single reference.	let myVariable = [1,'Bob','Steve',10];
Refer to each member of the array like this:
myVariable[0], myVariable[1], etc.

*Object*	This can be anything. Everything in JavaScript is an object and can be stored in a variable. Keep this in mind as you learn.	let myVariable = document.querySelector('h1');
All of the above examples too.