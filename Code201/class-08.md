# CSS Layout

## Learn CSS - Flexbox


-Flexbox is designed for one-dimensional content. Explain what this means.

The Flexible Box Layout Model (flexbox) is a layout model designed for one-dimensional content. It excels at taking a bunch of items which have different sizes, and returning the best layout for those items.

This is the ideal layout model for this sidebar pattern. Flexbox not only helps lay the sidebar and content out inline, but where there's not enough space remaining, the sidebar will break onto a new line. Instead of setting rigid dimensions for the browser to follow, with flexbox, you can instead provide flexible boundaries to hint how the content could display.

Features

They can display as a row, or a column.

They respect the writing mode of the document.

They are single line by default, but can be asked to wrap onto multiple lines.

Items in the layout can be visually reordered, away from their order in the DOM.

Space can be distributed inside the items, so they become bigger and smaller according to the space available in their parent.

Space can be distributed around the items and flex lines in a wrapped layout, using the Box Alignment properties.

The items themselves can be aligned on the cross axis.


-Explain the difference between the main axis and cross axis.

The key to understanding flexbox is to understand the concept of a main axis and a cross axis. The main axis is the one set by your flex-direction property. If that is row your main axis is along the row, if it is column your main axis is along the column.

The cross axis runs in the other direction to the main axis, so if flex-direction is row the cross axis runs along the column.

The main axis follows your flex-direction.

<div class="container" id="container">
  <div>One</div>
  <div>Item two</div>
  <div>The item we will refer to as three</div>
</div>


.container {
  display: flex;
}


-How can using certain properties of flexbox negatively impact accessibility?

The row-reverse and column-reverse values are a good example of this. The reordering only happens for the visual order, not the logical order. This is important to understand as the logical order is the order that a screen reader will read out the content, and anyone navigating using the keyboard will follow.

.container {
  display: flex;
  flex-wrap: wrap;
}

flex-grow: 0: items do not grow.
flex-shrink: 1: items can shrink smaller than their flex-basis.
flex-basis: auto: items have a base size of auto.

## CSS Layout - Flexbox

Read up to “Flex-Flow Shorthand”

What are some advantages of using flexbox over float?

Much more content, space control, and presentation control.


How does this topic connect with your long term goals?

It is a tool that I can use to visually display content in an organized way.



# Helpful Links

https://web.dev/learn/css/flexbox/

https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox

https://web.dev/learn/css/layout/

https://codepen.io/web-dot-dev/pen/gOgYqvz.css