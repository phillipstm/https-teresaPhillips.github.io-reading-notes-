# Read: 07 - Programming with JavaScript
- [Table of Contents](README.md)

control flow- the order in which the computer executes statements in a script.




Statements
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


Arithmetic operators are used to perform arithmetic on numbers:

Operator	Description
+	Addition
-	Subtraction
*	Multiplication
**	Exponentiation (ES2016)
/	Division
%	Modulus (Division Remainder)
++	Increment
--	Decrement


Assignment operators assign values to JavaScript variables.

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
