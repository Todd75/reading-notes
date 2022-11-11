# 301 Class Five Reading Notes "Putting it all together: Thinking In React"

## 5 Steps

1. Break The UI Into A Component Hierarchy
2. Build A Static Version in React
3. Identify The Minimal (but complete) Representation Of UI State
4. Identify Where Your State Should Live
5. Add Inverse Data Flow

## Questions

1. What is the single responsibility principle and how does it apply to components? The idea components ideally should only do one thing.
2. What does it mean to build a ‘static’ version of your application? A version that just renders your data before the functionality comes.
3. Once you have a static application, what do you need to add? You need to identify the minimum viable product(in working state).
4. What are the three questions you can ask to determine if something is state? Is it passed in from a parent via props? Does it remain unchanged over time? Can you compute it based on any other state or props in your component?
5. How can you identify where state needs to live? Identify every component that renders something based on that state, or find all cpmponents where something lives only in the component.
6. What is a “higher-order function”? Functions that operate on other functions, either by taking them as arguments or by returning them.
7. Explore the greaterThan function as defined in the reading. In your own words, what is line 2(`return m => m > n;`) of this function doing? It is searching over the array and will return number m if it is greater tha n.
8. Explain how either map or reduce operates, with regards to higher-order functions. The map method transforms an array by applying a function to all of its elements and building a new array from the returned values.

## Resources

- [Thinking in React](https://reactjs.org/docs/thinking-in-react.html)

- [Higher Order Functions](https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK)

## Return to the Table of Contents

[Table of Contents](https://todd75.github.io/reading-notes/)
