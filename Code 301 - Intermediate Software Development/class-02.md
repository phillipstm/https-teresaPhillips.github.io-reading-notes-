# React lifecycle
https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093


Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?

Render

What is the very first thing to happen in the lifecycle of React?

Mounting- When an instance of a component is being created and inserted into the DOM it occurs during the mounting phase. Constructor, static getDerivedStateFromProps, render, componentDidMount, and UNSAFE_componentWillMount all occur in this order during mounting

Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates

Constructor
Render
React Updates
componentDidMount, componentWill Unmount


What does componentDidMount do?

This method is invoked immediately after a component is mounted. If you need to load anything using a network request or initialize the DOM, it should go here. This method is a good place to set up any subscriptions. If you do that, don’t forget to unsubscribe in componentWillUnmount().


## React State Vs Props
https://www.youtube.com/watch?v=IYvD9oBCuJI

What types of things can you pass in the props?

Things that you want in a parent component, these are like variables. Information that really doesn't need updated.

What is the big difference between props and state?

The key difference between props and state is that state is internal and controlled by the component itself while props are external and controlled by whatever renders the component.

Props - Is like arguments to a function

State - always sets current state, and then second is parameter. Useful to update user info inide of a form.
There are three things you should know about setState().
  1. They don't modify State directly
  2. State updates may become asyncounous
  3. State updates are merged/


When do we re-render our application?


What are some examples of things that we could store in state?

User inputs to update, selections.

## Bookmark and Review


React Docs - State and Lifecycle
https://reactjs.org/docs/state-and-lifecycle.html

React Docs - handling events
https://reactjs.org/docs/handling-events.html

React Tutorial through ‘Developer Tools’
https://reactjs.org/tutorial/tutorial.html

React Bootstrap Documentation
https://react-bootstrap.github.io/

Boootstrap Cheatsheet
https://getbootstrap.com/docs/5.0/examples/cheatsheet/

Bootstrap Shuffle - a class “sandbox”
https://bootstrapshuffle.com/classes

Netlify
https://www.netlify.com/

## Things I want to know more about

Can only use Hooks inside function components.
Hooks always have to execute in the same order.
when using set state hooks and you need to previous render on a class you need ...previous state to pull all in