# Debugging

## What Went Wrong? Troubleshooting JavaScript.
https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_went_wrong

1. Name some key differences between a Syntax Error and a Logic Error

- Syntax errors: These are spelling errors in your code that actually cause the program not to run at all, or stop working part way through — you will usually be provided with some error messages too. These are usually okay to fix, as long as you are familiar with the right tools and know what the error messages mean!

- Logic errors: These are errors where the syntax is actually correct but the code is not what you intended it to be, meaning that program runs successfully but gives incorrect results. These are often harder to fix than syntax errors, as there usually isn't an error message to direct you to the source of the error.


2. List a few types of errors that you have encountered in past lab assignments and explain how you were able to correct them.

I have had several syntax errors: I was able to correct them by checking the console log on the web page. You shows you the type of error and where the error is located. I then went to my code and searched the line with the error until I could figure out the problem. It is usually missing a semi colon or a closing bracket.


3. How will this topic continue to influence your long term goals?

It gives me a better understanding of the developer lingo, in order to be able to find and fix the errors that occur.


# The JavaScript Debugger
https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_are_browser_developer_tools#the_javascript_debugger

1. How would you describe the JavaScript Debugger tool and how it works to someone just starting out in software development?

It is a resource that is available to you to help determine where your coding errors are and how to step into them and correct them using a break point. There are three parts to them they are:

-File list
The first pane on the left contains the list of files associated with the page you are debugging. Select the file you want to work with from this list. Click on a file to select it and view its contents in the center pane of the Debugger.

-Watch expressions and breakpoints
The right-hand pane shows a list of the watch expressions you have added and breakpoints you have set.

n the image, the first section, Watch expressions, shows that the listItems variable has been added. You can expand the list to view the values in the array.

The next section, Breakpoints, lists the breakpoints set on the page. In example.js, a breakpoint has been set on the statement listItems.push(inputNewItem.value);

The final two sections only appear when the code is running.

-Call stack section shows you what code was executed to get to the current line. You can see that the code is in the function that handles a mouse click, and that the code is currently paused on the breakpoint.

Scopes, shows what values are visible from various points within your code. 

2. Define what a breakpoint is.

A break point is a way to pause execution of the code in an order to determine where your code is breaking.


3. What is the call stack?

Call stack section shows you what code was executed to get to the current line. 



## Book Marks

Debugging HTML-https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Debugging_HTML

Debugging CSS-https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Debugging_CSS


## Things I want to know more about

Practice using the Dev Tools to gain a better understanding of thier usefulness.

