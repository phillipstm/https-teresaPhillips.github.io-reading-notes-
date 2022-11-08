# Redux - Combined Reducers

## Multiple Reducers Example

<https://www.youtube.com/watch?v=gBER4Or86hE>

**Why create multiple reducers?**

Redux reducers are great in that they are only aware of part of your data, and the rest of the data is neither reachable nor able to be mutated by your reducer.

**How would you combine multiple reducers?**

Import combineReducers from redux. Const each reducer in the file, within the index file there needs to be a function that combines the reducers.

**How will you manage state as an immutable object? why?**

You will want to create a new state of the object rather than mutate current state.

## Redux Docs: Using Combined Reducers

<https://redux.js.org/recipes/structuring-reducers/using-combinereducers/>

**combineReducers is a utility function to simplify the most common use case when writing ___ _____ .**

    Redux reducers

**Explain how combineReducers assembles the new state tree.**

In order to assemble the new state tree, combineReducers will call each slice reducer with its current slice of state and the current action, giving the slice reducer a chance to respond and update its slice of state if needed.

**How would you define initial state in an app using combineReducers?**

There are two ways to define the initial shape and contents of your store's state.

First, the createStore function can take preloadedState as its second argument. This is primarily intended for initializing the store with state that was previously persisted elsewhere, such as the browser's localStorage.

The other way is for the root reducer to return the initial state value when the state argument is undefined.

## Redux Docs: Combined Reducer Syntax

<https://redux.js.org/api/combinereducers/>

**Why will you want to split your reducing functions as your app becomes more complex?**

You'll want to split your reducing function into separate functions, each managing independent parts of the state.

**The _____ helper function turns an object whose values are different reducing functions into a single reducing function you can pass to ____.**

combineReducers
createStore

**What is a popular convention when naming reducers?**

A popular convention is to name reducers after the state slices they manage.

## Things I want to know more about

Notes
This function is mildly opinionated and is skewed towards helping beginners avoid common pitfalls. This is why it attempts to enforce some rules that you don't have to follow if you write the root reducer manually.

Any reducer passed to combineReducers must satisfy these rules:

For any action that is not recognized, it must return the state given to it as the first argument.

It must never return undefined. It is too easy to do this by mistake via an early return statement, so combineReducers throws if you do that instead of letting the error manifest itself somewhere else.

If the state given to it is undefined, it must return the initial state for this specific reducer. According to the previous rule, the initial state must not be undefined either. It is handy to specify it with ES6 optional arguments syntax, but you can also explicitly check the first argument for being undefined.
