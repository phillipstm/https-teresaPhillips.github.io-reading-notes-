# Component-Based Architecture
https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm


## 1.	What is a “component”?

A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface.

A component is a software object, intended to interact with other components, encapsulating certain functionality or a set of functionalities. It has an obviously defined interface and conforms to a recommended behavior common to all components within an architecture.

A software component can be defined as a unit of composition with a contractually specified interface and explicit context dependencies only. That is, a software component can be deployed independently and is subject to composition by third parties.

## 2.	What are the characteristics of a component?

Object-oriented view

A component is viewed as a set of one or more cooperating classes. Each problem domain class (analysis) and infrastructure class (design) are explained to identify all attributes and operations that apply to its implementation. It also involves defining the interfaces that enable classes to communicate and cooperate.


Conventional view

It is viewed as a functional element or a module of a program that integrates the processing logic, the internal data structures that are required to implement the processing logic and an interface that enables the component to be invoked and data to be passed to it.


Process-related view

In this view, instead of creating each component from scratch, the system is building from existing components maintained in a library. As the software architecture is formulated, components are selected from the library and used to populate the architecture.


## 3.	What are the advantages of using component-based architecture?

Ease of deployment − As new compatible versions become available, it is easier to replace existing versions with no impact on the other components or the system as a whole.

Reduced cost − The use of third-party components allows you to spread the cost of development and maintenance.
Ease of development − Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system.

Reusable − The use of reusable components means that they can be used to spread the development and maintenance cost across several applications or systems.

Modification of technical complexity − A component modifies the complexity through the use of a component container and its services.
Reliability − The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse.

System maintenance and evolution − Easy to change and update the implementation without affecting the rest of the system.
Independent − Independency and flexible connectivity of components. Independent development of components by different group in parallel. Productivity for the software development and future software development.


# What is Props and How to Use it in React
https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0#:~:text=%E2%80%9CProps%E2%80%9D%20is%20a%20special%20keyword,way%20from%20parent%20to%20child


## 1.	What is “props” short for?

“Props” is a special keyword in React, which stands for properties and is being used for passing data from one component to another.

## 2.	How are props used in React?

But the important part here is that data with props are being passed in a uni-directional flow. (one way from parent to child)
 Props data is read-only, which means that data coming from the parent should not be changed by child components.

## 3.	What is the flow of props?

Firstly, define an attribute and its value(data)
Then pass it to child component(s) by using Props
Finally, render the Props Data


Arguments passed to a function

const addition = (firstNum, secondNum) => { 
return firstNum + secondNum; 
};


Arguments passed to a React component:

const ChildComponent = (props) => { 
return <p>I'm the 1st child!</p>; 
};


Final Step: Rendering Props Data

{props}

console.log(props);

const ChildComponent = (props) => { 
return <p>{props.text}</p>; 
};

class ParentComponent extends Component { 
render() {
return (
<h1>
I'm the parent component.
<ChildComponent text={"I'm the 1st child"} />
<ChildComponent text={"I'm the 2nd child"} />
<ChildComponent text={"I'm the 3rd child"} />
</h1>
);
}
}



## Bookmark and Review

•	React Tutorial through ‘Passing Data Through Props’
https://reactjs.org/tutorial/tutorial.html

•	React Docs - Hello world
https://reactjs.org/docs/hello-world.html

•	React Docs - Introducing JSX
https://reactjs.org/docs/introducing-jsx.html

•	React Docs - Rendering elements
https://reactjs.org/docs/rendering-elements.html

•	React Docs - Components and props
https://reactjs.org/docs/components-and-props.html
