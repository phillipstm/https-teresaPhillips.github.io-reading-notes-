# Application State with Redux

## Dan Abramov Redux Tutorials

<https://egghead.io/courses/getting-started-with-redux>

**What is the first principle of Redux?**

Everything that changes in your app is contained in a single data script object which is state or the state tree.

**what is a store and what do we use our reducers for within that store?**

The store is a function that allows you to create state and pass argument of action. The reducer function takes state as [], and action as arguments. And takes a look at the action type. It then returns a new array.

**Name three Redux store methods given to us by createStore and describe their use.**

getState()
dispatch()
subscribe()

**Explain to a non-technical recruiter what combineReducers() does and why it is useful.**

It is a function that takes in only a object and generates the top level reducer for you. The object lets you specify the argument as the reducers you want to call. It is a single reducer that can call many reducers.

## Bookmark and Review

worlds easiest guide to redux <https://medium.freecodecamp.org/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6>

testing reducers <https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1>

Redux Docs <https://redux.js.org/>

## Things I want to know more about

All of it