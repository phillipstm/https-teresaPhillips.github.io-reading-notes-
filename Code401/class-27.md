# useState() Hook

## Introducing Hooks

<https://reactjs.org/docs/hooks-intro.html#motivation>

**What was the motivation for introducing Hooks?**

They let you use state and other React features without writing a class.
Hooks solve a wide variety of seemingly unconnected problems.
*Hooks allow you to reuse stateful logic without changing your component hierarchy.*
*Hooks let you split one component into smaller functions based on what pieces are related (such as setting up a subscription or fetching data)*
*Hooks let you use more of React’s features without classes.*

**What changes are important regarding implementing Hooks versus Component Classes?**

They let you use state and other React features without writing a class. You can use them in conjunction without rewriting your code.

**Hooks allow you to reuse stateful logic without changing ___ _______.**

 a  class.

## hooks api

<https://reactjs.org/docs/hooks-overview.html>

**Name two rules imposed by React Hook usage.**

Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions.

Only call Hooks from React function components. Don’t call Hooks from regular JavaScript functions. (There is just one other valid place to call Hooks — your own custom Hooks. We’ll learn about them in a moment.)

**How would you identify a custom Hook and why might you create one?**

It would start with use

## the state hook

<https://reactjs.org/docs/hooks-state.html>

**What is a Hook?**

A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components.

**When would I use the useState Hook?**

In a function component, we have no this, so we can’t assign or read this.state. Instead, we call the useState Hook directly inside our component

**If you were to add React state to a function component by declaring a state variable:**
    **What does calling useState do?****

        It declares a “state variable”. This is a way to “preserve” some values between the function calls — useState is a new way to use the exact same capabilities that this.state provides in a class. Normally, variables “disappear” when the function exits but state variables are preserved by React.

    **What do we pass to useState as an argument?**

        The only argument to the useState() Hook is the initial state.

    **What does useState return?**

        It returns a pair of values: the current state and a function that updates it.This is similar to this.state.count and this.setState in a class, except you get them in a pair. 
        ex:
        const [count, setCount] = useState()

## Bookmark and Review

**hooks api reference**<https://reactjs.org/docs/hooks-reference.html>

Learning Goals Reflection

To learn to efficiently use hooks in React.

## Things I want to know more about

Using hooks to in a app.
