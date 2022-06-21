# Introductory HTML and JavaScript


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

# Getting Started with HTML

## What is an HTML attribute?


## Describe the Anatomy of an HTMl element.
*The opening tag:* This consists of the name of the element (in this example, p for paragraph), wrapped in opening and closing angle brackets. This opening tag marks where the element begins or starts to take effect. In this example, it precedes the start of the paragraph text.
*The content:* This is the content of the element. In this example, it is the paragraph text.
*The closing tag:* This is the same as the opening tag, except that it includes a forward slash before the element name. This marks where the element ends. Failing to include a closing tag is a common beginner error that can produce peculiar result

<p>My cat is very grumpy</p>

*Nesting Elements*
Elements can be placed within other elements. This is called nesting. If we wanted to state that our cat is very grumpy, we could wrap the word very in a <strong> element, which means that the word is to have strong(er) text formatting:

<p>My cat is <strong>very</strong> grumpy.</p>

*Block vs Inline Elements*
Block-level elements form a visible block on a page. A block-level element appears on a new line following the content that precedes it. Any content that follows a block-level element also appears on a new line. Block-level elements are usually structural elements on the page. For example, a block-level element might represent headings, paragraphs, lists, navigation menus, or footers. A block-level element wouldn't be nested inside an inline element, but it might be nested inside another block-level element.
Inline elements are contained within block-level elements, and surround only small parts of the document's content (not entire paragraphs or groupings of content). An inline element will not cause a new line to appear in the document. It is typically used with text, for example an <a> element creates a hyperlink, and elements such as <em> or <strong> create emphasis.


<em>first</em><em>second</em><em>third</em>

<p>fourth</p><p>fifth</p><p>sixth</p>

<em> is an inline element. As you see below, the first three elements sit on the same line, with no space in between. On the other hand, <p> is a block-level element. Each p element appears on a new line, with space above and below. (The spacing is due to default CSS styling that the browser applies to paragraphs.)

firstsecondthird

fourth

fifth

sixth

*Empty Elements*
Some elements consist of a single tag, which is typically used to insert/embed something in the document. For example, the <img> element embeds an image file onto a page:

<img src="https://raw.githubusercontent.com/mdn/beginner-html-site/gh-pages/images/firefox-icon.png">


## What is the Difference between <article> and <section> element tags?

## What Elements does a “typical” website include?

## How does metadata influence Search Engine Optimization?


## How is the <meta> HTML tag used when specifying metadata?