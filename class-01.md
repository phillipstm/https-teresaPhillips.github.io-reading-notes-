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

*Attributes*
Elements can also have attributes. Attributes look like this:
<p class="editors note">My cat is very grumpy</p>

Attributes contain extra information about the element that won't appear in the content. In this example, the class attribute is an identifying name used to target the element with style information.

An attribute should have:
-A space between it and the element name. (For an element with more than one attribute, the attributes should be separated by spaces too.)
-The attribute name, followed by an equal sign.
-An attribute value, wrapped with opening and closing quote marks.

Another example of an element is <a>. This stands for *anchor*. An anchor can make the text it encloses into a hyperlink. Anchors can take a number of attributes, but several are as follows:

*href:* This attribute's value specifies the web address for the link. For example: href="https://www.mozilla.org/".
*title:* The title attribute specifies extra information about the link, such as a description of the page that is being linked to. For example, title="The Mozilla homepage". This appears as a tooltip when a cursor hovers over the element.
*target:* The target attribute specifies the browsing context used to display the link. For example, target="_blank" will display the link in a new tab. If you want to display the linked content in the current tab, just omit this attribute.

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

Note: In HTML, there is no requirement to add a / at the end of an empty element's tag, for example: <img src="images/cat.jpg" alt="cat" />. However, it is also a valid syntax and you may do this when you want your HTML to be valid XML.

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
  </head>
  <body>
    <p>This is my page</p>
  </body>
</html>

<!DOCTYPE html>: More recently, the doctype is a historical artifact that needs to be included for everything else to work right. <!DOCTYPE html> is the shortest string of characters that counts as a valid doctype. That is all you need to know!

<html></html>: The <html> element. This element wraps all the content on the page. It is sometimes known as the root element.
## What is the Difference between <article> and <section> element tags?

<head></head>: The <head> element. This element acts as a container for everything you want to include on the HTML page, that isn't the content the page will show to viewers. This includes keywords and a page description that would appear in search results, CSS to style content, character set declarations, and more.
## What Elements does a “typical” website include?

<meta charset="utf-8">: The <meta> element. This element represents metadata that cannot be represented by other HTML meta-related elements, like <base>, <link>, <script>, <style> or <title>. The charset attributes sets the character set for your document to UTF-8, which includes most characters from the vast majority of human written languages. With this setting, the page can now handle any textual content it might contain. There is no reason not to set this, and it can help avoid some problems later.

<title></title>: The <title> element. This sets the title of the page, which is the title that appears in the browser tab the page is loaded in. The page title is also used to describe the page when it is bookmarked.

<body></body>: The <body> element. This contains all the content that displays on the page, including text, images, videos, games, playable audio tracks, or whatever else.

## What is the Difference between <article> and <section> element tags?

<article> encloses a block of related content that makes sense on its own without the rest of the page (e.g., a single blog post).

<section> is similar to <article>, but it is more for grouping together a single part of the page that constitutes one single piece of functionality (e.g., a mini map, or a set of article headlines and summaries), or a theme. It's considered best practice to begin each section with a heading; also note that you can break <article>s up into different <section>s, or <section>s up into different <article>s, depending on the context.

## What Elements does a “typical” website include?

Href 
Meta 


## How does metadata influence Search Engine Optimization?

This element specifies the document's character encoding — the character set that the document is permitted to use. utf-8 is a universal character set that includes pretty much any character from any human language. This means that your web page will be able to handle displaying any language; it's therefore a good idea to set this on every web page you create! For example, your page could handle English and Japanese just fine:


## How is the <meta> HTML tag used when specifying metadata?

It is used a source tag

Now search for "MDN Web Docs" in your favorite search engine (We used Google.) You'll notice the description <meta> and <title> element content used in the search result — definitely worth having!

<meta name="description" content="The MDN Web Docs site
  provides information about Open Web technologies
  including HTML, CSS, and APIs for both Web sites and
  progressive web apps.">


# How to start to design a Website.

## What is the first step to designing a Website?

What exactly do I want to accomplish?
How will a website help me reach my goals?
What needs to be done, and in what order, to reach my goals?

## What is the most important question to answer when designing a Website?

What goal do you want your website to achieve

# Semantics
Semantics refers to the meaning of a piece of code

## Why should you use an <h1> element over a <span> element to display a top level heading?

 <h1> element is a semantic element, which gives the text it wraps around the role (or meaning) of "a top level heading on your page.
 <span> This will render it to look like a top level heading, but it has no semantic value, so it will not get any extra benefits as described above. It is therefore a good idea to use the right HTML element for the right job.


## What are the benefits of using semantic tags in our HTML?

 Some of the benefits from writing semantic markup are as follows:

Search engines will consider its contents as important keywords to influence the page's search rankings (see SEO)

Screen readers can use it as a signpost to help visually impaired users navigate a page

Finding blocks of meaningful code is significantly easier than searching through endless divs with or without semantic or namespaced classes

Suggests to the developer the type of data that will be populated

Semantic naming mirrors proper custom element/component naming

# What is JavaScript?

is a scripting language that enables you to create dynamically updating content, control multimedia, animate images, and pretty much everything else.

## Describe 2 things that require JavaScript in the Browser?

*Browser APIs* are built into your web browser, and are able to expose data from the surrounding computer environment, or do useful complex things. For example:

The DOM (Document Object Model) API allows you to manipulate HTML and CSS, creating, removing and changing HTML, dynamically applying new styles to your page, etc.
 Every time you see a popup window appear on a page, or some new content displayed (as we saw above in our simple demo) for example, that's the DOM in action.

The Geolocation API retrieves geographical information. This is how Google Maps is able to find your location and plot it on a map.

The Canvas and WebGL APIs allow you to create animated 2D and 3D graphics. People are doing some amazing things using these web technologies — see Chrome Experiments and webglsamples.

Audio and Video APIs like HTMLMediaElement and WebRTC allow you to do really interesting things with multimedia, such as play audio and video right in a web page, or grab video from your web camera and display it on someone else's computer (try our simple Snapshot demo to get the idea).

*Third party APIs* are not built into the browser by default, and you generally have to grab their code and information from somewhere on the Web. For example:

The Twitter API allows you to do things like displaying your latest tweets on your website.

The Google Maps API and OpenStreetMap API allows you to embed custom maps into your website, and other such functionality.

## How can you add JavaScript to an HTML document?

JavaScript is applied to your HTML page in a similar manner to CSS. Whereas CSS uses <link> elements to apply external stylesheets and <style> elements to apply internal stylesheets to HTML, JavaScript only needs one friend in the world of HTML — the <script> element. Let's learn how this works.

Internal JavaScript
First of all, make a local copy of our example file apply-javascript.html. Save it in a directory somewhere sensible.

Open the file in your web browser and in your text editor. You'll see that the HTML creates a simple web page containing a clickable button.

Next, go to your text editor and add the following in your head — just before your closing </head> tag:

<script>

  // JavaScript goes here

</script>

### Inline JavaScript handlers

 JavaScript code living inside HTML.

 function createParagraph() {
  const para = document.createElement('p');
  para.textContent = 'You clicked the button!';
  document.body.appendChild(para);
}

<button onclick="createParagraph()">Click me!</button>



<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8">
    <title>Apply JavaScript example</title>
  </head>
  <body>
    <button>Click me</button>
  </body>
</html>