# Course 201 Class Seven "Object-Oriented Programming, HTML Tables"

## Domain Modeling

Domain modeling is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.

To model the random nature of user behavior, you'll need the help of a random number generator. Fortunately, the JavaScript standard library includes a Math.random() function for just this sort of occasion.

`EpicFailVideo.prototype.generateRandom = function(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;`

## Tables

A table is a structured set of data made up of rows and columns (tabular data). A table allows you to quickly and easily look up values that indicate some kind of connection between different types of data.
The point of a table is that it is rigid. Information is easily interpreted by making visual associations between row and column headers.
Be under no illusion; for tables to be effective on the web, you need to provide some styling information with CSS, as well as good solid structure with HTML. In this module we are focusing on the HTML part; to find out about the CSS part you should visit our Styling tables article after you've finished here.





**Question One:**

1. Explain why we need domain modeling.

  We need domain modeling because it helps the arcitect govern the the development of an application more easily.

1. Why should tables not be used for page layouts?

  Tables shouldn't be used for page layouts anymore because CSS can better handle the layout. Tables reduce the screen readers information.

2. List and describe 3 different semantic HTML elements used in an HTML `<table>`.

  header, section, and article are three sematic elements used in tables.

## Constructors

Using object literals is fine when you only need to create one object, but if you have to create more than one, as in the previous section, they're seriously inadequate. We have to write out the same code for every object we create, and if we want to change some properties of the object - like adding a height property - then we have to remember to update every object.

`function createPerson(name) {

  const obj = {};

  obj.name = name;

  obj.introduceSelf = function () {

   console.log(`Hi! I'm ${this.name}.`);

  };

  return obj;
}`

This function creates and returns a new object each time we call it. The object will have two members:

a property name
a method introduceSelf().

**Questions:**

1. What is a constructor and what are some advantages to using it?

 A type of function used to create more than 1 Object it can be used as a template to create other objects. 

2. How does the term this differ when used in an object literal versus when used in a constructor?

 With an object literal this returns a single object, however in constructor function noation this can be instatiated into multiple instances.

 ## Object Prototypes

You can't get very far in JavaScript without dealing with objects. They're foundational to almost every aspect of the JavaScript programming language. In fact, learning how to create objects is probably one of the first things you studied when you were starting out. With that said, in order to most effectively learn about prototypes in JavaScript, we're going to channel our inner Jr. developer and go back to the basics.

Objects are key/value pairs. The most common way to create an object is with curly braces {} and you add properties and methods to an object using dot notation.

**Object.create:**
Let's improve our example once again by using Object.create. Simply put, Object.create allows you to create an object which will delegate to another object on failed lookups. Put differently, Object.create allows you to create an object and whenever there's a failed property lookup on that object, it can consult another object to see if that other object has the property.

The most important difference between class- and prototype- based inheritance is that class defines *type* which can be instantiated at runtime, whereas a prottype is itself an object instance.

**Questions:**

1. Explain prototypes and inheritance via an analogy from your previous work experience.

This I had an issue with as I dont understand it well myself.

## Thing I want to Know more About

1. Inheritance via prototypes vs classical

## Resources

[Domain Modeling](https://github.com/codefellows/domain_modeling#domain-modeling)

[HTML table Basics](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics)

[Constructors](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics#introducing_constructors)

[HTML Table Advanced](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics#introducing_constructors)

## Return to the Table of Contents

[Table of Contents](https://todd75.github.io/reading-notes/)
