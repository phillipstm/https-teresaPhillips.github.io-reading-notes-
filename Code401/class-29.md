# Advanced State with Reducers

## useReducer hook

<https://reactjs.org/docs/hooks-reference.html#usereducer>

**Name an alternative to the useState Hook.**

 useReducer(reducer, initialArg, init);

**Why might the useReducer Hook be preferable to the useState Hook?**

useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one.

useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.

**What are two ways to set the initial state?**

1.Specifying the initial state. The simplest way is to pass the initial state as a second argument:

  const [state, dispatch] = useReducer(
    reducer,
    {count: initialCount}
  );

2.Lazy initialization. You can also create the initial state lazily. To do this, you can pass an init function as the third argument. The initial state will be set to init(initialArg).

It lets you extract the logic for calculating the initial state outside the reducer. This is also handy for resetting the state later in response to an action.

## Ultimate Guide to useReducer

<https://blog.logrocket.com/guide-to-react-usereducer-hook/>

**In terms of state, what does useReducer expect to receive as a parameter?**

It accepts a reducer function as its first parameter and the initial state as the second.

**What does useReducer return?**

useReducer returns an array that holds the current state value and a dispatch function to which you can pass an action and later invoke it. While this is similar to the pattern Redux uses, there are a few differences.

**Explain dispatch to a non-technical recruiter.**

A store: An immutable object that holds the application’s state data
A reducer: A function that returns some state data, triggered by an action type
An action: An object that tells the reducer how to change the state. It must contain a type property and can contain an optional payload property

* Learning Goals... are the same as yesterday.

## Things I want to know more about

The reducer function
The **JavaScript** reduce() method executes a reducer function on each element of the array and returns a single value. The reduce() method accepts a reducer function, which itself can accept up to four arguments. The code snippet below illustrates how a reducer works

    const reducer = (accumulator, currentValue) => accumulator + currentValue;
    [2, 4, 6, 8].reduce(reducer)
    // expected output: 20

In **React**, useReducer essentially accepts a reducer function that returns a single value:

    const [count, dispatch] = useReducer(reducer, initialState);

The reducer function itself accepts two parameters and returns one value. The first parameter is the current state, and the second is the action. The state is the data we are manipulating. The reducer function receives an action, which is executed by a dispatch function:

    function reducer(state, action) { }

    dispatch({ type: 'increment' })