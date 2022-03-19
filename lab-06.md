# 06 - Dynamic web pages with JavaScript
- [Table of Contents](README.md)


JavaScript | MDN (mozilla.org)  or JS  just in time

JS) is a lightweight, interpreted, or just-in-time compiled programming language with first-class functions. . JavaScript is a prototype-based, multi-paradigm, single-threaded, dynamic language, supporting object-oriented, imperative, and declarative (e.g. functional programming) styles. Read more about JavaScript.

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide

Note: In JavaScript, all code instructions should end with a semi-colon (;) — your code may work correctly for single lines, but probably won't when you are writing multiple lines of code together. Try to get into the habit of including it.

## Components of JS

### variables
A variable is a container for a value, like a number we might use in a sum, or a string that we might use as part of a sentence.
-Notes-Variables are containers for storing values. It's a good programming practice to declare all variables at the beginning of a script.

    4 Ways to Declare a JavaScript Variable:

    Using var
    Using let
    Using const
    Using nothing

-Note always declare JavaScript variables with var,let, or const. The var keyword is used in all JavaScript code from 1995 to 2015. The let and const keywords were added to JavaScript in 2015. If you want your code to run in older browser, you must use var.

If you want a general rule: always declare variables with const. If you think the value of the variable can change, use let. In this example, price1, price2, and total, are variables:

    const price1 = 5;
    const price2 = 6;
    let total = price1 + price2;


    <button id="button_A">Press me</button>
    <h3 id="heading_A"></h3>

    const buttonA = document.querySelector('#button_A');
    const headingA = document.querySelector('#heading_A');

    buttonA.onclick = () => {
    const name = prompt('What is your name?');
    alert(`Hello ${name}, nice to see you!`);
    headingA.textContent = `Welcome ${name}`;
    }

### Numbers and operators
Combine operators and other features to successfully manipulate numbers to do our bidding.

Integers- are floating-point numbers without a fraction. They can either be positive or negative, e.g. 10, 400, or -5.

Floating point numbers (floats)- have decimal points and decimal places, for example 12.5, and 56.7786543.

Doubles- are a specific type of floating point number that have greater precision than standard floating point numbers (meaning that they are accurate to a greater number of decimal places).

Other types of number systems! Decimal is base 10 (meaning it uses 0–9 in each column), but we also have things like:

Binary — The lowest level language of computers; 0s and 1s.
Octal — Base 8, uses 0–7 in each column.
Hexadecimal — Base 16, uses 0–9 and then a–f in each column. You may have encountered these numbers before when setting colors in CSS.

const myInt = 5;
const myFloat = 6.667;
myInt;
myFloat;

Note--operator precedence — some operators are applied before others when calculating the result of a calculation (referred to as an expression, in programming). Operator precedence in JavaScript is the same as is taught in math classes in school

## Handling Text Strings

strings — this is what pieces of text are called in programming.

Declaring a variable, initializing it with a string value, and then returning the value. The only difference here is that when writing a string, you need to surround the value with quotes.

    const string = 'The revolution will not be televised.';
    console.log(string);

Escaping Strings-To fix previous problem code line, we need to escape the problem quote mark. Escaping characters means that we do something to them to make sure they are recognized as text, not part of the code. In JavaScript, we do this by putting a backslash just before the character.

    const bigmouth = 'I\'ve got no right to take my place...';
    console.log(bigmouth);

Conccontenating Strings-To join together strings in JavaScript you can use a different type of string, called a template literal. A template literal looks just like a normal string, but instead of using single or double quote marks (' or "), you use backtick characters (`):

    const name = 'Chris';
    const greeting = `Hello, ${name}`;
    console.log(greeting); // "Hello, Chris"

## Useful String Methods

Strings with built-in methods, such as finding the length of a text string, joining and splitting strings, substituting one character in a string for another, and more.

    const string = 'This is my string';

### Finding the length of a string
Use the length property. Try entering the following lines: Useful to find the lengths of a series of names so you can display them in order of length, or let a user know that a username they have entered into a form field is too long if it is over a certain length.

    const browserType = 'mozilla';
    browserType.length;

### Retrieving a specific string character
Return any character inside a string by using square bracket notation — this means you include square brackets ([]) on the end of your variable name. Inside the square brackets you include the number of the character you want to return.
        
    browserType[0];

## Remember: computers count from 0, not 1!

To retrieve the last character of any string, we could use the following line, combining this technique with the length property we looked at above:

    browserType[browserType.length-1];

### Testing if a string contains a substring
To find if a substring is inside a string. This can be done using the includes() method, which takes a single parameter — the substring you want to search for. It returns true if the string contains the substring, and false otherwise.

    const browserType = 'mozilla';

    if (browserType.includes('zilla')) {
    console.log('Found zilla!');
    } else {
    console.log('No zilla here!');
    }

To find if a string starts or ends with a particular substring. This is a common enough need that there are two special methods for this: startsWith() and endsWith():

    if (browserType.startsWith('zilla')) {
        or
    if (browserType.endsWith('zilla')) {

### Extracting a substring from a string
You can extract a substring from a string using the slice() method. The index at which to start extracting. The index at which to stop extracting. This is exclusive, meaning that the character at this index is not included in the extracted substring.

    const browserType = 'mozilla';
    console.log(browserType.slice(1, 4)); // "ozi"

If you want to extract all of the remaining characters in a string after a certain character, you don't have to include the second parameter. Instead, you only need to include the character position from where you want to extract the remaining characters in a string.

### Changing case
The string methods toLowerCase() and toUpperCase() take a string and convert all the characters to lower- or uppercase.

    const radData = 'My NaMe Is MuD';
    console.log(radData.toLowerCase());
    console.log(radData.toUpperCase());

### Updating parts of a string 
You can replace one substring inside a string with another substring using the replace() method. 

    const browserType = 'mozilla';
    const updated = browserType.replace('moz','van');

    console.log(updated);      // "vanilla"
    console.log(browserType);  // "mozilla"

-Note that replace(), like many string methods, doesn't change the string it was called on, but returns a new string. If you want to update the original browserType variable.
-Note we now have to declare browserType using let, not const, because we are reassigning it.

    let browserType = 'mozilla';
    browserType = browserType.replace('moz','van');

    console.log(browserType);  // "vanilla"














