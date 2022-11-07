# 301 Class One Reading Notes "Introduction to React and Components"

Component-based architecture focuses on the decomposition of the design into individual functional or logical components that represent well-defined communication interfaces containing methods, events, and properties. It provides a higher level of abstraction and divides the problem into sub-problems, each associated with component partitions.

A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface.

A component is a software object, intended to interact with other components, encapsulating certain functionality or a set of functionalities. It has an obviously defined interface and conforms to a recommended behavior common to all components within an architecture.

## Questions

1. What is a “component”? A component is modular, lightweight piece of code that is reusable and designed to be reduce coding time and costs.
2. What are the characteristics of a component? reuseable, replaceable, not content specific, extensible, independant, and encapsulated
3. What are the advantages of using component-based architecture? The components are reuseable, easier to deploy, cheaper, reliable, and make it easier to change or update your system.

## Props

React is a component-based library that divides the UI into little reusable pieces. In some cases, those components need to communicate (send data to each other) and the way to pass data between components is by using props.

“Props” is a special keyword in React, which stands for properties and is being used for passing data from one component to another.

But the important part here is that data with props are being passed in a uni-directional flow. (one way from parent to child)

Furthermore, props data is read-only, which means that data coming from the parent should not be changed by child components.

## Questions on Props

1. What is “props” short for? Props is short for properties that are used for passing data from one component to another.
2. How are props used in React? Firstly, define an attribute and its value(data), then pass it to child component(s) by using Props, and
finally render the Props Data.
3. What is the flow of props? The flow is props can only be passed to components in one way...Parent to Child

## Resources

- [Component Based Architecture](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm)

- [What is “Props” and how to use it in React?](https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0)

## Return to the Table of Contents

[Table of Contents](https://todd75.github.io/reading-notes/)
