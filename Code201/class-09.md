# HTML Forms
https://developer.mozilla.org/en-US/docs/Learn/Forms/Your_first_form


-Why are forms so important in web development?

They provide the structure to the entire website.


-When designing a form, what are some key things to keep in mind when it comes to user experience?

That it needs to be well structured for all users. Using the correct element enables accessability readers to inturpet the data correctly'

-List 5 form elements and explain their importance.

The < form> element formally defines a form and attributes that determine the form's behavior.

The < fieldset> element is a convenient way to create groups of widgets that share the same purpose, for styling and semantic purposes. 

Many assistive technologies will use the < legend> element as if it is a part of the label of each control inside the corresponding < < < fieldset> element. For example, some screen readers such as Jaws and NVDA will speak the legend's content before speaking the label of each control.

The < label> element is the formal way to define a label for an HTML form widget. This is the most important element if you want to build accessible forms — when implemented properly, screenreaders will speak a form element's label along with any related instructions, as well as it being useful for sighted users.

The < button> HTML element is an interactive element activated by a user with a mouse, keyboard, finger, voice command, or other assistive technology. Once activated, it then performs a programmable action, such as submitting a form or opening a dialog.


# Learn JS- Event Listeners
https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events

-How would you describe events to a non-technical friend?

Events are actions or occurrences that happen in the system you are programming, which the system tells you about so your code can react to them.

-When using the addEventListener() method, what 2 arguments will you need to provide?

addEventListener() method, that takes at least two arguments: the name of the event and a function to handle the event. 


-Describe the event object. Why is the target within the event object useful?

The event object, and it is automatically passed to event handlers to provide extra features and information. Here you can see we are including an event object, e, in the function, and in the function setting a background color style on e.target — which is the button itself. The target property of the event object is always a reference to the element the event occurred upon.


-What is the difference between event bubbling and event capturing?

Event bubbling and capture are terms that describe phases in how the browser handles events targeted at nested elements.

In the capturing phase:

The browser checks to see if the element's outer-most ancestor (< html>) has a click event handler registered on it for the capturing phase, and runs it if so.
Then it moves on to the next element inside < html> and does the same thing, then the next one, and so on until it reaches the direct parent of the element that was actually clicked.

In the bubbling phase, the exact opposite of the capturing phase occurs:

The browser checks to see if the direct parent of the clicked element has a click event handler registered on it for the bubbling phase, and runs it if so.
Then it moves on to the next immediate ancestor element and does the same thing, then the next one, and so on until it reaches the <html> element.


# Bookmark and Review

https://developer.mozilla.org/en-US/docs/Learn/Forms/HTML5_input_types

https://developer.mozilla.org/en-US/docs/Web/Events


## Things I want to know more about

html form controls. 
event listeners