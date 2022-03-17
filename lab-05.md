# Read: 05 - Design web pages with CSS

CSS is a language for specifying how documents are presented to users — how they are styled, laid out, etc.
h1 {
    color: red;
    font-size: 5em;
}
The rule opens with a selector . This selects the HTML element that we are going to style. In this case we are styling level one headings (<h1>).
We then have a set of curly braces { }. Inside those will be one or more declarations, which take the form of property and value pairs. Each pair specifies a property of the element(s) we are selecting, then a value that we'd like to give the property.

CSS reference https://www.w3schools.com/css/default.asp

3 ways to insert CSS

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

