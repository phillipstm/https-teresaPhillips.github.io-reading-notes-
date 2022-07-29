# React Docs - Thinking in React
<https://reactjs.org/docs/thinking-in-react.html>

**What is the single responsibility principle and how does it apply to components?**

A component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.

Don’t use state at all to build this static version. State is reserved only for interactivity, that is, data that changes over time. Since this is a static version of the app, you don’t need it.

**What does it mean to build a ‘static’ version of your application?**

To build a version that takes your data model and renders the UI but has no interactivity.


**Once you have a static application, what do you need to add?**

Add the components of your data table as

FilterableProductTable
SearchBar
ProductTable
ProductCategoryRow
ProductRow

**What are the three questions you can ask to determine if something is state?**

Is it passed in from a parent via props? If so, it probably isn’t state.

Does it remain unchanged over time? If so, it probably isn’t state.

Can you compute it based on any other state or props in your component? If so, it isn’t state.


**How can you identify where state needs to live?**

For each piece of state in your application:

Identify every component that renders something based on that state.

Find a common owner component (a single component above all the components that need the state in the hierarchy).

Either the common owner or another component higher up in the hierarchy should own the state.

If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.


## Higher-Order Functions
<https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK>


**What is a “higher-order function”?**

Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions.

Higher-order functions allow us to abstract over actions, not just values. They come in several forms.


**Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?**

Line 2 is showing us that m is greater than n.


function greaterThan(n) {
  return m => m > n;
}
let greaterThan10 = greaterThan(10);
console.log(greaterThan10(11));
// → true

**Explain how either map or reduce operates, with regards to higher-order functions.**

Being able to pass function values to other functions is a deeply useful aspect of JavaScript. It allows us to write functions that model computations with “gaps” in them. The code that calls these functions can fill in the gaps by providing function values.

**Arrays** provide a number of useful higher-order methods. You can use **forEach** to loop over the elements in an array. The **filter method** returns a new array containing only the elements that pass the predicate function. Transforming an array by putting each element through a function is done with **map**. You can use **reduce** to combine all the elements in an array into a single value. The **some method** tests whether any element matches a given **predicate function**. And **findIndex** finds the position of the first element that matches a predicate.


### Things I want to know more about

Learning more functions and how to apply them.
Learning more built in functions and how they work.