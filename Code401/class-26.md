# Component Based UI

## react hello world

<https://facebook.github.io/react/docs/hello-world.html>

**What are the building blocks of a React app?**

Element and Components

**What is the difference between an element and a React component?**

Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain React and JavaScript.

**Elements** are the smallest building blocks of React apps.
An element describes what you want to see on the screen.
Unlike browser DOM elements, React elements are plain objects, and are cheap to create.
Elements are what components are “made of”.
React elements are immutable.
Once you create an element, you can’t change its children or attributes.
An element is like a single frame in a movie: it represents the UI at a certain point in time.

**Components** Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.
The simplest way to define a component is to write a JavaScript function: This function is a valid React component because it accepts a single “props” (which stands for properties) object argument with data and returns a React element.
When React sees an element representing a user-defined component, it passes JSX attributes and children to this component as a single object. We call this object “props”.

function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

const root = ReactDOM.createRoot(document.getElementById('root'));
const element = <Welcome name="Sara" />;
root.render(element);

Let’s recap what happens in this example:

We call root.render() with the <Welcome name="Sara" /> element.
React calls the Welcome component with {name: 'Sara'} as the props.
Our Welcome component returns a <h1>Hello, Sara</h1> element as the result.
React DOM efficiently updates the DOM to match <h1>Hello, Sara</h1>.

Components can refer to other components in their output. A button, a form, a dialog, a screen

**What are some advantages of React’s component based architecture**?

## introducing JSX

<https://facebook.github.io/react/docs/introducing-jsx.html>

**What is JSX and why do we use it?**

It is called JSX, and it is a syntax extension to JavaScript.

**Describe the process of embedding JavaScript expressions in JSX.**
**Is it safe to embed user input in JSX? Explain.**

## rendering elements

<https://facebook.github.io/react/docs/rendering-elements.html>

**Explain what a React Component is to a non-technical friend.**
**Describe mutability and React Components, specifically, how is the UI updated?**
**If changes are made to the UI, what does React update?**

## Bookmark and Review

**sass cheatsheet**<https://devhints.io/sass>
**react cheatsheet**<https://devhints.io/react>
**another react cheatsheet**<https://reactcheatsheet.com/>

## Additional Questions

**Looking ahead at this module’s course schedule, What do you look forward to learning?**
**What are your learning goals after reading and reviewing the class README?**

## Things I want to know more about

