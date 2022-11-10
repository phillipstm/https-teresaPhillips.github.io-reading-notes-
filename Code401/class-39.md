# Redux - Additional Topics

## Redux Toolkit (RTK)

<https://redux-toolkit.js.org/introduction/getting-started>

**What concerns are addressed by Redux Toolkit?**

"Configuring a Redux store is too complicated"
"I have to add a lot of packages to get Redux to do anything useful"
"Redux requires too much boilerplate code"

**What does configureStore() do?**

configureStore(): wraps createStore to provide simplified configuration options and good defaults. It can automatically combine your slice reducers, adds whatever Redux middleware you supply, includes redux-thunk by default, and enables use of the Redux DevTools Extension.

**How would I use createSlice()?**

createSlice(): accepts an object of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types.

## MobX

<https://mobx.js.org/getting-started.html>

**What is Mobx?**

A simple, scalable and battle tested state management solution.
MobX is a standalone library, but most people are using it with React

**How does MobX make it “impossible” to produce an inconsistent state?**

First of all, there is the application state. Graphs of objects, arrays, primitives, references that forms the model of your application. These values are the “data cells” of your application.

Secondly there are derivations. Basically, any value that can be computed automatically from the state of your application. These derivations, or computed values, can range from simple values, like the number of unfinished todos, to complex stuff like a visual HTML representation of your todos. In spreadsheet terms: these are the formulas and charts of your application.

Reactions are very similar to derivations. The main difference is these functions don't produce a value. Instead, they run automatically to perform some task. Usually this is I/O related. They make sure that the DOM is updated or that network requests are made automatically at the right time.

Finally there are actions. Actions are all the things that alter the state. MobX will make sure that all changes to the application state caused by your actions are automatically processed by all derivations and reactions. Synchronously and glitch-free.

**How would we build a reactive user interface?**

The observer HoC wrapper from the mobx-react-lite package fixes that by basically wrapping the React component in autorun. This keeps the component in sync with the state. This is conceptually not different from what we did with the report before.

The only MobX specific code in there is the observer wrapping. That is enough to make sure that each component individually re-renders when relevant data changes

## Tutorial

<https://redux-toolkit.js.org/tutorials/intermediate-tutorial>

**What take-away(s) did this tutorial provide?**

Create Store-
Create a file named src/app/store.js. Import the configureStore API from Redux Toolkit.
This creates a Redux store, and also automatically configure the Redux DevTools extension so that you can inspect the store while developing.

Provider-
make it available to our React components by putting a React-Redux <Provider> around our application in src/index.js. Import the Redux store we just created, put a <Provider> around your <App>, and pass the store as a prop:

Slice-
A file named src/features/counter/counterSlice.js. In that file, import the createSlice API from Redux Toolkit.
Creating a slice requires a string name to identify the slice, an initial state value, and one or more reducer functions to define how the state can be updated. Once a slice is created, we can export the generated Redux action creators and the reducer function for the whole slice.

Add Slice Reducer to Store-
We need to import the reducer function from the counter slice and add it to our store. By defining a field inside the reducer parameter, we tell the store to use this slice reducer function to handle all updates to that state.

Redux State and Actions-
React-Redux hooks to let React components interact with the Redux store. We can read data from the store with useSelector, and dispatch actions using useDispatch. Create a src/features/counter/Counter.js file with a <Counter> component inside, then import that component into App.js and render it inside of <App>.

features/counter/Counter.js
import React from 'react'
import { useSelector, useDispatch } from 'react-redux'
import { decrement, increment } from './counterSlice'

export function Counter() {
  const count = useSelector((state) => state.counter.value)
  const dispatch = useDispatch()

  return (
    <div>
      <div>
        <button
          aria-label="Increment value"
          onClick={() => dispatch(increment())}
        >
          Increment
        </button>
        <span>{count}</span>
        <button
          aria-label="Decrement value"
          onClick={() => dispatch(decrement())}
        >
          Decrement
        </button>
      </div>
    </div>
  )
}

## Things I want to know more about

Redux Toolkit also includes a powerful data fetching and caching capability that we've dubbed "RTK Query". It's included in the package as a separate set of entry points. It's optional, but can eliminate the need to hand-write data fetching logic yourself.
