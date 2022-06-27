# Object-Oriented Programming, HTML Tables

## Domain Modeling

Explain why we need domain modeling.

A domain model that's articulated well can verify and validate the understanding of a specific problem among various stakeholders. As a communication tool, it defines a vocabulary that can be used within and between both technical and business teams.

Domain modeling is the process of creating a conceptual model for a specific problem. And a domain model that's articulated well can verify and validate your understanding of that problem.

Here's some tips to follow when building your own domain models.

When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.

Model its attributes with a constructor function that defines and initializes properties.

Model its behaviors with small methods that focus on doing one job well.

Create instances using the new keyword followed by a call to a constructor function.

Store the newly created object in a variable so you can access its properties and methods from outside.

Use the this variable within methods so you can access the object's properties and methods from inside.


## HTML Table Basics

https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics

Why should tables not be used for page layouts?

Layout tables reduce accessibility for visually impaired users: Screenreaders, used by blind people, interpret the tags that exist in an HTML page and read out the contents to the user. Because tables are not the right tool for layout, and the markup is more complex than with CSS layout techniques, the screenreaders' output will be confusing to their users.

Tables produce tag soup: As mentioned above, table layouts generally involve more complex markup structures than proper layout techniques. This can result in the code being harder to write, maintain, and debug.

Tables are not automatically responsive: When you use proper layout containers (such as <header>, <section>, <article>, or <div>), their width defaults to 100% of their parent element. Tables on the other hand are sized according to their content by default, so extra measures are needed to get table layout styling to effectively work across a variety of devices.


List and describe 3 different semantic HTML elements used in an HTML <table>

<td> The smallest container inside a table is a table cell, which is created by a <td> element ('td' stands for 'table data').

<td>Hi, I'm your first cell.</td>
<td>I'm your second cell.</td>
<td>I'm your third cell.</td>
<td>I'm your fourth cell.</td>


<tr> To stop this row from growing and start placing subsequent cells on a second row, we need to use the <tr> element ('tr' stands for 'table row').

<tr>
  <td>Hi, I'm your first cell.</td>
  <td>I'm your second cell.</td>
  <td>I'm your third cell.</td>
  <td>I'm your fourth cell.</td>
</tr>

<th> To recognize the table headers as headers, both visually and semantically, you can use the <th> element ('th' stands for 'table header'). This works in exactly the same way as a <td>, except that it denotes a header, not a normal cell. Go into your HTML, and change all the <td> elements surrounding the table headers into <th> elements.

<table>
  <tr>
    <th>Animals</th>
  </tr>
  <tr>
    <th>Hippopotamus</th>
  </tr>
  <tr>
    <th>Horse</th>
    <td>Mare</td>
  </tr>
  <tr>
    <td>Stallion</td>
  </tr>
  <tr>
    <th>Crocodile</th>
  </tr>
  <tr>
    <th>Chicken</th>
    <td>Hen</td>
  </tr>
  <tr>
    <td>Rooster</td>
  </tr>
</table>




## Introducing Constructors

What is a constructor and what are some advantages to using it?

Set of methods and the properties it can have — and then create as many objects as we like, just updating the values for the properties that are different.

A better way is to use a constructor. A constructor is just a function called using the new keyword. When you call a constructor, it will:

create a new object
bind this to the new object, so you can refer to this in your constructor code
run the code in the constructor
return the new object.
Constructors, by convention, start with a capital letter and are named for the type of object they create. So we could rewrite our example like this:

function Person(name) {
  this.name = name;
  this.introduceSelf = function() {
    console.log(`Hi! I'm ${this.name}.`);
  }
}


How does the term this differ when used in an object literal versus when used in a constructor?

Built in objects and APIs don't always create object instances automatically. As an example, the Notifications API — which allows modern browsers to fire system notifications — requires you to instantiate a new object instance using the constructor for each notification you want to fire.

## Object Prototypes Using A Constructor

Explain prototypes and inheritance via an analogy from your previous work experience.
NOTE: This is a very common front end developer interview question


## Bookmark and Review

HTML Table Advanced Features and Accessibility
https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Advanced