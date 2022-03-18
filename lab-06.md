# 06 - Dynamic web pages with JavaScript


JavaScript | MDN (mozilla.org)  or JS  just in time

JS) is a lightweight, interpreted, or just-in-time compiled programming language with first-class functions. . JavaScript is a prototype-based, multi-paradigm, single-threaded, dynamic language, supporting object-oriented, imperative, and declarative (e.g. functional programming) styles. Read more about JavaScript.

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide

Note: In JavaScript, all code instructions should end with a semi-colon (;) — your code may work correctly for single lines, but probably won't when you are writing multiple lines of code together. Try to get into the habit of including it.

## Components of JS

### variables
A variable is a container for a value, like a number we might use in a sum, or a string that we might use as part of a sentence.

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




