# Course 201 Class Six "Problem Domain, Objects, and the DOM"

## JavaScript object basics

An object is a collection of related data and/or functionality. These usually consist of several variables and functions (which are called properties and methods when they are inside objects).
As with many things in JavaScript, creating an object often begins with defining and initializing a variable.

An object is made up of multiple members, each of which has a name, and a value. Each name/value pair must be separated by a comma, and the name and value in each case are separated by a colon. The syntax always follows this pattern:

    const objectName = {
      member1Name: member1Value,
      member2Name: member2Value,
      member3Name: member3Value,
    }; 

The value of an object member can be pretty much anything. Numbers, arrays, functions etc
*An object like this is referred to as an object literal — we've literally written out the object contents as we've come to create it. This is different compared to objects instantiated from classes, which we'll look at later on.*

It is very common to create an object using an object literal when you want to transfer a series of structured, related data items in some manner, for example sending a request to the server to be put into a database. Sending a single object is much more efficient than sending several items individually, and it is easier to work with than an array, when you want to identify individual items by name.

### bracket notation

Bracket notation provides an alternative way to access object properties.

### What is the DOM?

The Document Object Model (DOM) is a programming interface for web documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects; that way, programming languages can interact with the page.

A web page is a document that can be either displayed in the browser window or as the HTML source. In both cases, it is the same document but the Document Object Model (DOM) representation allows it to be manipulated. As an object-oriented representation of the web page, it can be modified with a scripting language such as JavaScript.

All of the properties, methods, and events available for manipulating and creating web pages are organized into objects. For example, the document object that represents the document itself, any table objects that implement the HTMLTableElement DOM interface for accessing HTML tables, and so forth, are all objects.

The DOM is built using multiple APIs that work together. The core DOM defines the entities describing any document and the objects within it. This is expanded upon as needed by other APIs that add new features and capabilities to the DOM. For example, the HTML DOM API adds support for representing HTML documents to the core DOM, and the SVG API adds support for representing SVG documents.





**Questions**

1. How would you describe an object to a non-technical friend you grew up with?

Think of it like it car... a car has different rims, paint, sizes, models ... well an object is like that car where it can have different properties related to it with in it.

2. What are some advantages to creating object literals?

They are easier to work with than arrays and work well for sending structured related data items.

3. How do objects differ from arrays?

They can be easier to work with than arrays. And arrays store data numerically in an index.

4. Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.

When the object properties name is hel in a variable.

5. Evaluate the code below. What does the term this refer to and what is the advantage to using this?

this refers to dog in the code.

1. What is the DOM?

DOM stands for document object model and it is an interface for web documents. The DOM allows the webpage to be maunipulated.

2. Briefly describe the relationship between the DOM and JavaScript.

They have a symbiotic relationship where Javascript needs the DOM to be able to display models or notaions of websites. 


***References:***

- [JavaScript Objects Basics](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics)
- [Introduction to the Dom](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)

Return to the Table of Contents: [Table of Contents](https://todd75.github.io/reading-notes/)
