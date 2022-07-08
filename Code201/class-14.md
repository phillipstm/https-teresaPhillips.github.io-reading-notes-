# CSS Transforms, Transitions, and Animations


## CSS Transforms
http://learn.shayhowe.com/advanced-html-css/css-transforms/


1. What does a CSS transform allow the developer to do to an element?

Transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values. With alternative ways to size, position, and change elements.

Transform Syntax

Transform property includes multiple vendor prefixes to gain the best support across all browsers. The un-prefixed declaration comes last to overwrite the prefixed versions, should a browser fully support the transform property

div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}


2D Transforms https://www.css3files.com/transform-rotate/

Elements may be distorted, or transformed, on both a two-dimensional plane or a three-dimensional plane. Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes. Three-dimensional transforms work on both the x and y axes, as well as the z axis. These three-dimensional transforms help define not only the length and width of an element, but also the depth.



2. Provide an example of a transform and how you could see that being used on a website.

2-D Scale I could see you using in order to grab a readers attention to the page, by having something important that you want to make sure the see.

HTML

<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>

              
CSS

.box-1 {
  transform: scale(.75);
}
.box-2 {
  transform: scale(1.25);
}



## CSS Transitions & Animations
http://learn.shayhowe.com/advanced-html-css/transitions-animations/


1. What does a CSS transition allow the developer to do to an element?

 The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes.

 There are four transition related properties in total, including transition-property, transition-duration, transition-timing-function, and transition-delay. Not all of these are required to build a transition, with the first three are the most popular.

 -example below the box will change its background color over the course of 1 second in a linear fashion.

 .box {
  background: #2db34a;
  transition-property: background;
  transition-duration: 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}


2. How does a CSS animation differ from a CSS transition?

Transitions do a great job of building out visual interactions from one state to another, and are perfect for these kinds of single state changes. However, when more control is required, transitions need to have multiple states. In return, this is where animations pick up where transitions leave off.


## 8 simple CSS3 transitions that will wow your users
http://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users


1. What are some benefits to using CSS transitions on websites?

Transition effect that will excite your users, increase engagement and ultimately, when used well, increase your conversions.

2. How this topic fit in with your long-term goals?

I'm not sure. But it would be fun to learn how to do some of these things.



### Book Marks

Pure CSS Bounce Animation
http://codepen.io/dp_lewis/pen/gCfBv


6 Buttons animated
http://codepen.io/retyui/pen/ByoaXV


CSS3 Animations: Keyframes
http://codepen.io/akshaychauhan/pen/oAfae


404
http://codepen.io/kieranfivestars/pen/MYdQxX



### Things I want to know more about

The State of JS   http://stateofjs.com/

2018 Stack Overflow Developer Survey  https://insights.stackoverflow.com/survey/2018

How it Feels to Learn JS in 2016  https://hackernoon.com/how-it-feels-to-learn-javascript-in-2016-d3a717dd577f#.ygr5pmdqy

String methods  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String

Array methods  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array

IIFEs

D.R.Y.

Basics of "pass by value" vs. "pass by reference"   hhttps://codeburst.io/explaining-value-vs-reference-in-javascript-647a975e12a0ttps://codeburst.io/explaining-value-vs-reference-in-javascript-647a975e12a0

Prototypal inheritance  

Scopes & closures

Node

Suggested JS readings

Eloquent JavaScript   http://eloquentjavascript.net/
You Don't Know JS     http://shop.oreilly.com/product/9780596517748.do
Eric Elliott's articles on Medium  https://medium.com/@_ericelliott
What is "this" in JavaScript?  https://www.javascripttutorial.net/javascript-this/
