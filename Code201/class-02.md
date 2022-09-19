## Introduction to HTML
# Read: 02 - HTML Text, CSS Introduction, and Basic JavaScript Instructions

### Why is it important to use semantic elements in our HTML?

One of HTML's main jobs is to give text meaning (also known as semantics), so that the browser knows how to display it correctly.

### How many levels of headings are there in HTML?

There are 6 levels of headings

### What are some uses for the <sup> and <sub> elements?

You will occasionally need to use superscript and subscript when marking up items like dates, chemical formulae, and mathematical equations so they have the correct meaning. The <sup> and <sub> elements handle this job.

<sup> is used for characters that should be subscript, suffixes, dates, mathematical concepts like raising a number to a power.

<sub> is used to contain charaters that should be subscript. Used for footnotes, chemical formulas as H<sub>2</sub>O


### When using the <abbr> element, what attribute must be added to provide the full expansion of the term?

The Title must be used.

<abbr> — this is used to wrap around an abbreviation or acronym, and provide a full expansion of the term (included inside a title attribute.)

<p>We use <abbr title="Hypertext Markup Language">HTML</abbr> to structure our web documents.</p>

<p>I think <abbr title="Reverend">Rev.</abbr> Green did it in the kitchen with the chainsaw.</p>

It will look like

We use HTML to structure our web documents.

I think Rev. Green did it in the kitchen with the chainsaw.

## Learn CSS

### What are ways we can apply CSS to our HTML?

three methods of applying CSS to a document: with an external stylesheet, with an internal stylesheet, and with inline styles.

*External* You reference an external CSS stylesheet from an HTML <link> element:

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>

The href attribute of the <link> element needs to reference a file on your file system. In the example above, the CSS file is in the same folder as the HTML document, but you could place it somewhere else and adjust the path. Here are three examples:

<!-- Inside a subdirectory called styles inside the current directory -->
<link rel="stylesheet" href="styles/style.css">

<!-- Inside a subdirectory called general, which is in a subdirectory called styles, inside the current directory -->
<link rel="stylesheet" href="styles/general/style.css">

<!-- Go up one directory level, then inside a subdirectory called styles -->
<link rel="stylesheet" href="../styles/style.css">

*Internal* stylesheet resides within an HTML document. To create an internal stylesheet, you place CSS inside a <style> element contained inside the HTML <head>.

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
    <style>
      h1 {
        color: blue;
        background-color: yellow;
        border: 1px solid black;
      }

      p {
        color: red;
      }
    </style>
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>


### Why should we avoid using inline styles?

Problomatic for sites with more than one page, an internal stylesheet becomes a less efficient way of working. To apply uniform CSS styling to multiple pages using internal stylesheets, you must have an internal stylesheet in every web page that will use the styling. The efficiency penalty carries over to site maintenance too. With CSS in internal stylesheets, there is the risk that even one simple styling change may require edits to multiple web pages.

### Review the block of code below and answer the following questions:

A selector targets HTML to apply styles to content. We have already discovered a variety of selectors in the Getting started with CSS tutorial. If CSS is not applying to content as expected, your selector may not match the way you think it should match.

Each CSS rule starts with a selector — or a list of selectors — in order to tell the browser which element or elements the rules should apply to. All the examples below are valid selectors or lists of selectors.

h1
a:link
.manythings
#onething
*
.box p
.box p:first-child
h1, h2, .intro


    What is representing the selector? h2

    Which components are the CSS declarations?

    CSS declaration blocks are paired with selectors to produce CSS rulesets (or CSS rules). The example below contains two rules: one for the h1 selector and one for the p selector. The colored highlighting identifies the h1 rule.

    all the h2 selector components

    Which components are considered properties?

    Color, padding


    Properties: These are human-readable identifiers that indicate which stylistic features you want to modify. For example, font-size, width, background-color.

     h2 {
     color: black;
     padding: 5px;
   }

   ## Learn JS


### What data type is a sequence of text enclosed in single quote marks?
A string

### List 4 types of JavaScript operators.

Addition +
Subtraction, Division, Multiplication -, /, *
Assingmemt =
Strict equal ===

### Describe a real world Problem you could solve with a Function.

Math problems



https://chris.beams.io/posts/git-commit/


## Things I want to know more about

all of it!
Citing, favicon, CSS, eventlisteners
