# Read: 05 - Design web pages with CSS

CSS is a language for specifying how documents are presented to users — how they are styled, laid out, etc.
h1 {
    color: red;
    font-size: 5em;
}
The rule opens with a selector . This selects the HTML element that we are going to style. In this case we are styling level one headings (<h1>).
We then have a set of curly braces { }. Inside those will be one or more declarations, which take the form of property and value pairs. Each pair specifies a property of the element(s) we are selecting, then a value that we'd like to give the property.

## Adding CSS to your document. 

To link styles.css to index.html, add the following line somewhere inside the <head> of the HTML document:

<link rel="stylesheet" href="styles.css">

CSS reference https://www.w3schools.com/css/default.asp to reference index of syntax

33 ways to insert CSS

External- styles are defined within the <link> element, inside the <head> section of an HTML page:

<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="mystyle.css">
</head>

Internal- styles are defined within the <style> element, inside the <head> section of an HTML page:

<!DOCTYPE html>
<html>
<head>
<style>
body {
  background-color: linen;
}

h1 {
  color: maroon;
  margin-left: 40px;
}
</style>
</head>

Inline- styles are defined within the "style" attribute of the relevant element:

<!DOCTYPE html>
<html>
<body>

<h1 style="color:blue;text-align:center;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>

</body>
</html>

## CSS HTML elements

To target all paragraphs in the document, you would use the selector p. To turn all paragraphs green, you would use:

p {
  color: green;
}

You can target multiple selectors at the same time by separating the selectors with a comma. If you want all paragraphs and all list items to be green, your rule would look like this:

p, li {
    color: green;
}

## Changing Default behavior

Choose the HTML element that you want to change and using a CSS rule to change the way it looks. A good example is <ul>, an unordered list. It has list bullets. If you don't want those bullets, you can remove them like so:

li {
  list-style-type: none;
}

## Adding a Class

Find a way to select a subset of the elements without changing the others. The most common way to do this is to add a class to your HTML element and target that class.

In your HTML document, add a class attribute to the second list item. Your list will now look like this:

<ul>
  <li>Item one</li>
  <li class="special">Item two</li>
  <li>Item <em>three</em></li>
</ul>

## Styling based on location within document

There are a number of selectors that can help you here, but for now we will look at just a couple. In our document, there are two <em> elements — one inside a paragraph and the other inside a list item. To select only an <em> that is nested inside an <li> element, you can use a selector called the descendant combinator, which takes the form of a space between two other selectors.

li em {
  color: rebeccapurple;
}

Something else you might like to try is styling a paragraph when it comes directly after a heading at the same hierarchy level in the HTML. To do so, place a + (an adjacent sibling combinator) between the selectors.

h1 + p {
  font-size: 200%;
}

## Styling based on State

a:link {
  color: pink;
}

a:visited {
  color: green;
}


## Combining Selectors and Contributors

/* selects any <span> that is inside a <p>, which is inside an <article>  */
article p span { ... }

/* selects any <p> that comes directly after a <ul>, which comes directly after an <h1>  */
h1 + ul + p { ... }

Multi types also

body h1 + p .special {
  color: yellow;
  background-color: black;
  padding: 5px;
}

## CSS Reset

https://meyerweb.com/eric/tools/css/reset/

