# Operators and Loops
- [Table of Contents](README.md)

## Assignment operators
An assignment operator assigns a value to its left operand based on the value of its right operand. The simple assignment operator is equal (=), which assigns the value of its right operand to its left operand. That is, x = f() is an assignment expression that assigns the value of f() to x. 

### Name	                Shorthand operator	        Meaning
Assignment	                 x = f()	                x = f()
Addition assignment	         x += f()	            x = x + f()
Subtraction assignment	     x -= f()	            x = x - f()
Multiplication assignment	 x *= f()	            x = x * f()
Division assignment	         x /= f()	            x = x / f()
Remainder assignment	     x %= f()	            x = x % f()
Exponentiation assignment	 x **= f()	            x = x ** f()
Left shift assignment	     x <<= f()	            x = x << f()
Right shift assignment	     x >>= f()	            x = x >> f()
Unsigned right shift assignment	x >>>= f()	        x = x >>> f()
Bitwise AND assignment	     x &= f()	            x = x & f()
Bitwise XOR assignment	     x ^= f()	            x = x ^ f()
Bitwise OR assignment	     x |= f()	            x = x | f()
Logical AND assignment	     x &&= f()	            x && (x = f())
Logical OR assignment	     x ||= f()	            x || (x = f())
Logical nullish assignment	 x ??= f()	            x ?? (x = f())

## Assigning to properties
If a variable refers to an object, then the left-hand side of an assignment expression may make assignments to properties of that variable. For example: 

    let obj = {};

    obj.x = 3;
    console.log(obj.x); // Prints 3.
    console.log(obj); // Prints { x: 3 }.

    const key = "y";
    obj[key] = 5;
    console.log(obj[key]); // Prints 5.
    console.log(obj); // Prints { x: 3, y: 5 }.

### Destructuring
For more complex assignments, the destructuring assignment syntax is a JavaScript expression that makes it possible to extract data from arrays or objects using a syntax that mirrors the construction of array and object literals.

    var foo = ['one', 'two', 'three'];

    // without destructuring
    var one   = foo[0];
    var two   = foo[1];
    var three = foo[2];

    // with destructuring
    var [one, two, three] = foo;

### Evaluation and nesting
Assignments are used within a variable declaration (i.e., with const, let, or var) or as standalone statements). Like other expressions, assignment expressions like x = f() evaluate into a result value. Although this result value is usually not used, it can then be used by another expression. 

-NOTE-Chaining assignments or nesting assignments in other expressions can result in surprising behavior. For this reason, some JavaScript style guides discourage chaining or nesting assignments).

By chaining or nesting an assignment expression, its result can itself be assigned to another variable. It can be logged, it can be put inside an array literal or function call, and so on.

    // Declares a variable x and initializes it to the result of f().
    // The result of the x = f() assignment expression is discarded.
    let x = f();

    // Declares a variable x and initializes it to the result of g().
    // The result of the x = g() assignment expression is discarded.
    x = g(); // Reassigns the variable x to the result of g().

    let x;
    const y = (x = f()); // Or equivalently: const y = x = f();
    console.log(y); // Logs the return value of the assignment x = f().

    console.log(x = f()); // Logs the return value directly.

    // An assignment expression can be nested in any place
    // where expressions are generally allowed,
    // such as as array literals' elements or as function calls' arguments.
    console.log([ 0, x = f(), 0 ]);
    console.log(f(0, x = f(), 0));

In the case of logical assignments, x &&= f(), x ||= f(), and x ??= f(), the return value is that of the logical operation without the assignment, so x && f(), x || f(), and x ?? f(), respectively.

When chaining these expressions without parentheses or other grouping operators like array literals, the assignment expressions are grouped right to left (they are right-associative), but they are evaluated left to right.

### Avoid assignment chains
In particular, putting a variable chain in a const, let, or var statement often does not work. Only the outermost/leftmost variable would get declared; any other variables within the assignment chain are not declared by the const/let/var statement. 

    let z = y = x = f();

This statement seemingly declares the variables x, y, and z. However, it only actually declares the variable z. y and x are either invalid references to nonexistent variables (in strict mode) or, worse, would implicitly create global variables for x and y in sloppy mode.

## Comparison operators
A comparison operator compares its operands and returns a logical value based on whether the comparison is true. The operands can be numerical, string, logical, or object values. Strings are compared based on standard lexicographical ordering, using Unicode values. In most cases, if the two operands are not of the same type, JavaScript attempts to convert them to an appropriate type for the comparison. This behavior generally results in comparing the operands numerically. The sole exceptions to type conversion within comparisons involve the === and !== operators, which perform strict equality and inequality comparisons. These operators do not attempt to convert the operands to compatible types before checking equality. The following table describes the comparison operators in terms of this sample code: 

    var var1 = 3;
    var var2 = 4;

###                      Comparison operators
Operator	            Description	                                                                      Examples returning true
Equal (==)	            Returns true if the operands are equal.	                                                            3 == var1
                                                                                                                          "3" == var1
                                                                                                                            3 == '3'
Not equal (!=)	        Returns true if the operands are not equal.	                                                    var1 != 4
                                                                                                                        var2 != "3"
Strict equal (===)	    Returns true if the operands are equal and of the same type. See also Object.is and sameness in JS.	3 === var1
Strict not equal (!==)	Returns true if the operands are of the same type but not equal, or are of different type.	    var1 !== "3"
3 !== '3'
Greater than (>)	    Returns true if the left operand is greater than the right operand.	                             var2 > var1
                                                                                                                         "12" > 2
Greater than or equal (>=)	Returns true if the left operand is greater than or equal to the right operand.	             var2 >= var1
                                                                                                                         var1 >= 3
Less than (<)	         Returns true if the left operand is less than the right operand.	                             var1 < var2
                                                                                                                          "2" < 12
Less than or equal (<=)	 Returns true if the left operand is less than or equal to the right operand.	                 var1 <= var2
                                                                                                                         var2 <= 5   

###-Note: => is not a comparison operator but rather is the notation for Arrow functions.                                                                                                                        

### Logical Operators

Operator	        Description	            Example	
&&	                    and	            (x < 10 && y > 1) is true	
||	                    or	            (x == 5 || y == 5) is false	
!	                    not	            !(x == y) is true

### Conditional (Ternary) Operator 
JavaScript also contains a conditional operator that assigns a value to a variable based on some condition. 
-Syntax
    variablename = (condition) ? value1:value2 

    let voteable = (age < 18) ? "Too young":"Old enough";

## Loops
Loops offer a quick and easy way to do something repeatedly. This chapter of the JavaScript Guide introduces the different iteration statements available to JavaScript. 

There are many different kinds of loops, but they all essentially do the same thing: they repeat an action some number of times. (Note that it's possible that number could be zero!)

# for statement loop
A for loop repeats until a specified condition evaluates to false. The JavaScript for loop is similar to the Java and C for loop. 

for - loops through a block of code a number of times

    for ([initialExpression]; [conditionExpression]; [incrementExpression])
    statement

-The initializing expression initialExpression, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression can also declare variables.

-The conditionExpression expression is evaluated. If the value of conditionExpression is true, the loop statements execute. If the value of condition is false, the for loop terminates. (If the condition expression is omitted entirely, the condition is assumed to be true.)

-The statement executes. To execute multiple statements, use a block statement ({ ... }) to group those statements.

-If present, the update expression incrementExpression is executed. 

-Control returns to Step 2.. 

# while loop
A while statement executes its statements as long as a specified condition evaluates to true.

while - loops through a block of code while a specified condition is true 

If the condition becomes false, statement within the loop stops executing and control passes to the statement following the loop.

The condition test occurs before statement in the loop is executed. If the condition returns true, statement is executed and the condition is tested again. If the condition returns false, execution stops, and control is passed to the statement following while.

To execute multiple statements, use a block statement ({ ... }) to group those statements. 

The following while loop iterates as long as n is less than 3:

    let n = 0;
    let x = 0;
    while (n < 3) {
    n++;
    x += n;
    }

With each iteration, the loop increments n and adds that value to x. Therefore, x and n take on the following values:

-After the first pass: n = 1 and x = 1
-After the second pass: n = 2 and x = 3
-After the third pass: n = 3 and x = 6
After completing the third pass, the condition n < 3 is no longer true, so the loop terminates.

### Infinite Loops-BAD, VERY VERY BAD
Avoid infinite loops. Make sure the condition in a loop eventually becomes false—otherwise, the loop will never terminate! The statements in the following while loop execute forever because the condition never becomes false:

    // Infinite loops are bad!
    while (true) {
    console.log('Hello, world!');
    }



