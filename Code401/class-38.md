# Redux - Asynchronous Actions

## async actions

<https://redux.js.org/advanced/asyncactions>

**Why use Redux middleware?**
 Redux middleware can do anything when it sees a dispatched action: log something, modify the action, delay the action, make an async call, and more. Also, since middleware form a pipeline around the real store.dispatch function, this also means that we could actually pass something that isn't a plain action object to dispatch, as long as a middleware intercepts that value and doesn't let it reach the reducers.

**Consider the Redux Async Data Flow Diagram. Describe the flow in your own words.**

The store sends an action to UI it passes it to Dispatch which sends it to the middleware where a request and response are sent to the API back to the Middleware which is then dispatched through the reducer and updates state.

**How are we accommodating async in our Redux app?**

With writing dispatch functions in our middleware.

## thunk middleware

<https://github.com/reduxjs/redux-thunk>

**Why would you need redux-thunk middleware?**

Thunks allow us to write additional Redux-related logic separate from a UI layer. This logic can include side effects, such as async requests or generating random values, as well as logic that requires dispatching multiple actions or access to the Redux store state.

**Redux Thunk middleware allows you to write action creators that return a ____ instead of an action.**

function

**Describe how any return value from the inner thunk function will be made available.**

The inner function will be called with each action as it's passed through the middleware chain.

## Things I want to know more about

All of it.