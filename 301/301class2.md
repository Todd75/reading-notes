# 301 Class Two Reading Notes "State and Props"

React lets you define components as classes or functions. The methods that you are able to use on these are called lifecycle events. These methods can be called during the lifecycle of a component, and they allow you to update the UI and application states.

Mounting, Updating, and Unmounting are the three phases of the component lifecycle.

## Mounting

When an instance of a component is being created and inserted into the DOM it occurs during the mounting phase. Constructor, static getDerivedStateFromProps, render, componentDidMount, and UNSAFE_componentWillMount all occur in this order during mounting.

### Questions

- Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’? componentDidMount is first before rendering unless there is rendering during the mounting phase the rendering happens first. Is there always rendering in the mounting phase?

- What is the very first thing to happen in the lifecycle of React? The constructor is called before it is mounted.

- Put the following things in the order that they happen: Constructor, Render in Mounting, Component Did Mount, then we go through the Updating phase of should it update, Render in Updating Phase, React update in Updating Phase, finally component will un mount.

- What does componentDidMount do? It is a method that is invoked after a compnent is mounted. A good spot to set subscriptions(dont forget to unsubscribe in unmount) Can connect API here.

### Props v State Questions

- What types of things can you pass in the props? Props are arguements to a function... so pass in anything that is handled outside of the component or updated outside of the component like initial count for a counter component. 

- What is the big difference between props and state? State is handled inside the component and doesn't get passed into the component, but props are handled outside the component and need to be passed inside of it.

- When do we re-render our application? After a prop has been passed in and the state has been updated assuming we have a prop to pass in.

- What are some examples of things that we could store in state? User inputs from forms like submit, checkbox, click events.

## Resources

- [React Component Life Cycle Events](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093)

- [React State v Props Video](https://www.youtube.com/watch?v=IYvD9oBCuJI)

## Return to the Table of Contents

[Table of Contents](https://todd75.github.io/reading-notes/)
