# Read: 07 - Programming with JavaScript

- [Table of Contents](../README.md)

control flow- the order in which the computer executes statements in a script.

## Statements
JavaScript statements and declarations

Control flow

Block
Empty statement
break
continue
if...else
switch
throw
try...catch

Declarations

var
let
const

Functions and classes

function
function*
async function
return
class

Iterations

do...while
for
for...in
for...of
for await...of
while

Other

debugger
export
import
label
with

if...else statement
Use the if statement to execute a statement if a logical condition is true. Use the optional else clause to execute a statement if the condition is false.

An if statement looks like this:

  if (condition) {
    statement_1;
  } else {
    statement_2;
  }

Boolean

  if (condition_1) {
    statement_1;
  } else if (condition_2) {
    statement_2;
  } else if (condition_n) {
    statement_n;
  } else {
    statement_last;
  }

Best practice

In general, it's good practice to always use block statements—especially when nesting if statements:

  if (condition) {
    statement_1_runs_if_condition_is_true;
    statement_2_runs_if_condition_is_true;
  } else {
    statement_3_runs_if_condition_is_false;
    statement_4_runs_if_condition_is_false;
  }


## Arithmetic operators are used to perform arithmetic on numbers:

Operator	Description
+	Addition
-	Subtraction
*	Multiplication
**	Exponentiation (ES2016)
/	Division
%	Modulus (Division Remainder)
++	Increment
--	Decrement


## Assignment operators assign values to JavaScript variables.

Operator	Example	  Same As
  =	     	x = y		  x = y
  +=	  	x += y		x = x + y
  -=		  x -= y		x = x - y
  *=		  x *= y		x = x * y
  /=		  x /= y		x = x / y
  %=		  x %= y		x = x % y
  <<=		  x <<= y		x = x << y
  >>=		  x >>= y		x = x >> y
  >>>=		x >>>= y	x = x >>> y
  &=		  x &= y		x = x & y
  ^=		  x ^= y		x = x ^ y
  |=		  x |= y		x = x | y
  **=		  x **= y		x = x ** y


## JavaScript functions
A JavaScript function is a block of code designed to perform a particular task. A JavaScript function is executed when "something" invokes it (calls it). Why use functions? You can reuse code: Define the code once, and use it many times. You can use the same code many times with different arguments, to produce different results.

A JavaScript function is defined with the function keyword, followed by a name, followed by parentheses ().
The parentheses may include parameter names separated by commas:
(parameter1, parameter2, ...)
The code to be executed, by the function, is placed inside curly brackets: {}

  function name(parameter1, parameter2, parameter3) {
  // code to be executed
  }

Function parameters are listed inside the parentheses () in the function definition.
Function arguments are the values received by the function when it is invoked.
Inside the function, the arguments (the parameters) behave as local variables.

### Function Invocation
The code inside the function will execute when "something" invokes (calls) the function:
When an event occurs (when a user clicks a button)
When it is invoked (called) from JavaScript code
Automatically (self invoked)

### Function Return
When JavaScript reaches a return statement, the function will stop executing.
If the function was invoked from a statement, JavaScript will "return" to execute the code after the invoking statement.
Functions often compute a return value. The return value is "returned" back to the "caller":

  let x = myFunction(4, 3);   // Function is called, return value will end up in x

  function myFunction(a, b) {
    return a * b;             // Function returns the product of a and b
  }

## The () Operator Invokes the Function
Using the example, toCelsius refers to the function object, and toCelsius() refers to the function result. Accessing a function without () will return the function object instead of the function result.

  function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
  }
  document.getElementById("demo").innerHTML = toCelsius(77);

*when invoked

  function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
  }
  document.getElementById("demo").innerHTML = toCelsius;

## Functions Used as Variable Values
Functions can be used the same way as you use variables, in all types of formulas, assignments, and calculations.

Instead of using a variable to store the return value of a function:

  let x = toCelsius(77);
  let text = "The temperature is " + x + " Celsius";

You can use the function directly, as a variable value:

  let text = "The temperature is " + toCelsius(77) + " Celsius";

## Local Variables
Variables declared within a JavaScript function, become LOCAL to the function. Local variables can only be accessed from within the function.
Since local variables are only recognized inside their functions, variables with the same name can be used in different functions. Local variables are created when a function starts, and deleted when the function is completed.

  // code here can NOT use carName

  function myFunction() {
    let carName = "Volvo";
    // code here CAN use carName
  }

  // code here can NOT use carName
