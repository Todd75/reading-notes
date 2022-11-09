# 301 Class Three Reading Notes "Passing Functions as Props"

Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity
When you don’t have stable IDs for rendered items, you may use the item index as a key as a last resort.

We don’t recommend using indexes for keys if the order of items may change. This can negatively impact performance and may cause issues with component state. Check out Robin Pokorny’s article for an in-depth explanation on the negative impacts of using an index as a key. If you choose not to assign an explicit key to list items then React will default to using indexes as keys.

## Key Questions

1. What does .map() return? It returns a new array.

2. If I want to loop through an array and display each value in JSX, how do I do that in React? You would use the map() method. 

3. Each list item needs a unique ____. Key.

4. What is the purpose of a key? A key is used to help React identify what has changed, added, or removed.

## Spead Operator Questions

1. What is the spread operator? It is useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.

2. List 4 things that the spread operator can do. Copy an array, combine an array, combine objects, add item to a list, or add to state to react.

3. Give an example of using the spread operator to combine two arrays.
`const myArray = [1,2,3]`

`const yourArray = [x,y,z]`

`const ourArray = [...myArray, ...yourArray]` is how

4. Give an example of using the spread operator to add a new item to an array.

`const dog = [3,4,5,6,7]`

`dog[0] = 2 would add the 2 to the 0 slot in the array`

5. Give an example of using the spread operator to combine two objects into one.

`const objectOne = {hello: "emoji"}`

`const obectTwo = {bacon: "emoji"}`

`const objectThjree = {...objectOne, ...objectTwo}`

## Video Questions

1. In the video, what is the first step that the developer does to pass functions between components? He creates a function near the state he wants to change

2. In your own words, what does the increment function do? It will increment the passed in data by one if you used ++

3. How can you pass a method from a parent component into a child component? it is passed as a prop to the child

4. How does the child component invoke a method that was passed to it from a parent component? 

## Resources

- [List and Keys](https://reactjs.org/docs/lists-and-keys.html)

- [How to Use the Spread Operator (…) in JavaScript](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

- [How to pass function between components Video](https://www.youtube.com/watch?v=c05OL7XbwXU)

## Return to the Table of Contents

[Table of Contents](https://todd75.github.io/reading-notes/)
