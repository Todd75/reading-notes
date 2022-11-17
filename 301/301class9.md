# 301 Class Nine Reading Notes "Functional Programming"

The first fundamental concept we learn when we want to understand functional programming is pure functions.

- It returns the same result if given the same arguments (it is also referred as deterministic)
- It does not cause any observable side effects

**If our function reads external files, it’s not a pure function — the file’s contents can change.**

- What is functional programming?  A style of programming that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data
- What is a pure function and how do we know if something is a pure function? It is a function that returns the same result if given the same arguements.
- What are the benefits of a pure function? It doesn't cause observable side-effects and is easier to test
- What is immutability? it means the function will not change over time
- What is Referential transparency? when a function consistently has the same output for the input it is called referential transparency
- What is a module? a small independant code block or javascript file
- What does the word ‘require’ do? It includes modules that exist in seperate files
- How do we bring another module into the file the we are working in? by calling it 
- What do we have to do to make a module available? we have to export the module set equal to what we want available outside the module

## Resources

- [Concepts of Functional Programming in Javascript](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

- [Node.JS Video](https://www.youtube.com/watch?v=xHLd36QoS4k)

## Return to the Table of Contents

[Table of Contents](https://todd75.github.io/reading-notes/)
