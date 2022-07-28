# React and Forms

## React Docs - Forms
<https://reactjs.org/docs/forms.html>


1. What is a ‘Controlled Component’?

In React, mutable state is typically kept in the state property of components, and only updated with setState().

We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.


2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.

Update the state as soon as they enter this way you could pass the information back to the parent state to notify all the children if needed.

3. How do we target what the user is entering if we have an event handler on an input field?

With bind?

## The Conditional (Ternary) Operator Explained
<https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff>


Shorten your if statements into one line of code with the conditional operator. Using a conditional, like an if statement, allows us to specify that a certain block of code should be executed if a certain condition is met.


We have a person object that consists of a name, age, and driver property.

let person = {
  name: 'tony',
  age: 20,
  driver: null
};

Test if the age of our person is greater than or equal to 16. If this is true, they’re old enough to drive and driver should say 'Yes'. If this is not true, driver should be set to 'No'.

if (person.age >= 16) {
  person.driver = 'Yes';
} else {
  person.driver = 'No';
}

**person.driver = person.age >=16 ? 'Yes' : 'No';**

**condition ? value if true : value if false**

4. Why would we use a ternary operator?

To check that a condition is met as an if statement.

5. Rewrite the following statement using a ternary statement:

if(x===y){
  console.log(true);
} else {
  console.log(false);
}

value.x = value.y === ? 'true' : ' false';

### Bookmark and Review

React Bootstrap - Forms  
<https://react-bootstrap.github.io/forms/overview/>

React Docs - conditional rendering
<https://reactjs.org/docs/conditional-rendering.html>>


### Things I want to know more about

Ace Your Javascript Interview — Learn Algorithms + Data Structures.
<https://codeburst.io/ace-your-javascript-interview-learn-algorithms-data-structures-dabb547fb385>