# Table of Contents
- [React](#What-is-React?)
- [Dom](#What-is-Dom?)
- [ES6](#What-is-ES6?)
- [Jsx](#What-is-JSX?)
- [Components](#What-are-Components?)
- [ClassComponents](#What-is-a-Class-Component?)
- [FunctionalComponents](#What-is-a-Functional-Component?)
- [Rendering](#What-is-rendering-a-component?)
- [Props](#What-is-Props?)
- [State](#What-is-State-in-React?)
- [ReactCss](#How-to-Use-CSS-in-React?)
- [Event](#What-is-react-event?)
- [List](#what-is-react-list?)
- [UseofKeys](#What-is-use-of-Keys-in-react?)
- [Memo](#What-is-memo?)
- [Redux](#What-is-Redux?)
- [React-Router](#What-is-React-Router?)
- [React-Contaxt](#What-is-React-Context?)
- [Hooks](#What-is-Hooks?)
- [useState](#What-is-useState?)
- [useEffect](#What-is-useEffect?)
- [useRef](#What-is-useRef?)
- [useReducer](#What-is-useReducer?)
- [useCallback](#What-is-useCallback?)
- [useMemo](#What-is-useMemo?)
- [Diff-useCallback-useMemo](#what-is-difference-between-useCallback-and-useMemo?)
- [Custom-Hooks](#What-is-custom-hooks?)

# What-is-React?
- React is refer as js framework.
- Created by Facebook.
- It's a tool of building UI components.
- It's work as Virtual Dom in memory.
- It's use as unidirectional one way data binding.

# What-is-Dom?
- Dom is stand for Document Object model.
- The representation of entire user interface of a web application as a tree data structure.
- It's classify as two parts (a)Virtual Dom  (b)Real Dom

# What-is-ES6?
- ES6 stands for ECMAScript 6.
    ## Classes
    - A class is a type of function, but instead of using the keyword function to initiate it,
     we use the keyword class, and the properties are assigned inside a constructor() method.
    - Methods of classes
      - To create a class inheritance, use the `extends` keyword.
      - The `super()` method refers to the parent class.
                class Car {
                  constructor(name) {
                    this.brand = name;
                  }
                }
                const mycar = new Car("Ford");
      - With a regular function, this represents the object that called the function.

    ## Arrow Functions
    - Arrow functions allow us to write shorter function syntax.
                  hello = () => {
                      return "Hello World!";
                  }
        
    ## Variables
       Var
      - If you use var outside of a function, it belongs to the global scope.
      - If you use var inside of a function, it belongs to that function.
      - If you use var inside of a block, i.e. a for loop, the variable is still available outside of that block.
      - var has a function scope, not a block scope.

       Let
      - let is the block scoped version of var, and is limited to the block (or expression) where it is defined.
      - If you use let inside of a block, i.e. a for loop, the variable is only available inside of that loop.
      - let has a block scope.

       Const
      - const is a variable that once it has been created, its value can never change.
      - const has a block scope.
      
    ## Destructuring
    - When destructuring arrays, the order that variables are declared is important.
    ```js
    const vehicles = ['mustang', 'f-150', 'expedition'];
    const [car, truck, suv] = vehicles;
    ```
    ## Spread Operator
    - The JavaScript spread operator (...) allows us to quickly copy all or part of an existing array or object into another array or object.
                  const numbersOne = [1, 2, 3];
                  const numbersTwo = [4, 5, 6];
                  const numbersCombined = [...numbersOne, ...numbersTwo];
    ## Modules
    - JavaScript modules allow you to break up your code into separate files.
    - This makes it easier to maintain the code-base.
    - ES Modules rely on the import and export statements.

    ## Ternary Operator
    - The ternary operator is a simplified conditional operator like if / else.
    - Syntax: `condition ? <expression if true> : <expression if false>`

                  authenticated ? renderApp() : renderLogin();

# What-is-JSX?
- JSX enables and simplifies the creation of HTML in React.
- JSX stands for JavaScript XML.
- JSX converts HTML tags into react elements.
- JSX you can write expressions inside curly braces { }.
- JSX is a JavaScript Extension Syntax used in React to easily write HTML and JavaScript together.
```js
const jsx = <h1>This is JSX</h1>
```
# What-are-Components?
- Components are like functions that return HTML elements.
- Components are independent and reusable bits of code. 
  They serve the same purpose as JavaScript functions, but work in isolation and return HTML.
- There are two kinds of components in React: functional and class components.

# What-is-a-Class-Component?
- Class components are ES6 classes that return JSX and necessitate the use of React extensions.
```js
            import React, { Component } from 'react'
            export default class App extends Component {
            render() {
            return (
                  <div>
                  <h1>Hello World</h1>
                  </div>
            )
            }
            }
```
# What-is-a-Functional-Component?
- A Function component also returns HTML, and behaves much the same way as a Class component,
  but Function components can be written using much less code, are easier to understand.
- A JavaScript/ES6 function that returns a React element is referred to as a functional component (JSX).
- Since the introduction of React Hooks, we have been able to use states in functional components.
```js
            function Car() {
            return <h2>Hi, I am a Car!</h2>;
            }
```
# What-is-rendering-a-component?
- Back Example of React application has a component called Car, which returns an `<h2>` element.
- To use of this component in your application, use similar syntax as normal HTML: `<Car />`
```js
            const root = ReactDOM.createRoot(document.getElementById('root'));
            root.render(<Car />);
```
# What-is-Props?
- Props are like function arguments, and you send them into the component as attributes in html.
- Components can be passed as props, which stands for properties.
- They are used to transfer data from one component to the next (parent component to child component).
- They are typically used to render dynamically generated data.
```js
            function Car(props) {
            return <h2>I am a {props.color} Car!</h2>;
            }
            const root = ReactDOM.createRoot(document.getElementById('root'));
            root.render(<Car color="red"/>);
```
# What-is-State-in-React?
- State is a built-in React Object that is used to create and manage data within our components.
  It differs from props in that it is used to store data rather than pass data.
- State is mutable (data can change) and accessible through this.state().
```js
            class App extends React.Component {
            constructor(props) {
            super(props);
            this.state = {
                  name: "John Doe"
            };
            }
            render() {
            return (
                  <div>
                  <h1>My name is {this.state.name}</h1>
                  </div>
            );
            }
            }
```
# How-to-Use-CSS-in-React?
- There are 3 ways to style a react application with CSS:
   - Inline Styles
   - External Styling
   - CSS in JS

# What-is-react-event?
- React has the same events as HTML: click, change, mouseover etc.
- React events are written in camelCase syntax: `onClick` instead of `onclick`.
- React event handlers are written inside curly braces: `onClick={damm}`  instead of `onClick="damm()"`.
- To pass an argument to an event handler, use an arrow function.

# What-is-react-list?
- In React, you will render lists with some type of loop. In the array method map() is generally the preferred method.

# What-is-use-of-Keys-in-react?
- Keys allow React to keep track of elements. 
- If an item is updated or removed, only that item will be re-rendered instead of the entire list.
- Keys need to be unique to each sibling. But they can be duplicated globally.

# What-is-memo?
- Using memo will cause React to skip rendering a component if its props have not changed.This can improve performance.

# What-is-Redux?
- Redux is a popular open-source JavaScript library for managing and centralizing application state.
  It is commonly used with React or any other view-library.

# What-is-React-Router?
- React router is a standard library used in React applications to handle routing and 
  allow navigation between views of various components.

# What-is-React-context?
- React context allows us to pass down and use (consume) data in whatever component 
  we need in our React app without using props.

# What-is-Hooks?
- Hooks were added to React in version 16.8.
- Hooks can only be called inside React function components.
- Hooks can only be called at the top level of a component.
- Hooks cannot be conditional.

# What-is-useState?
- The React useState Hook allows us to track state in a function component.
- State generally refers to data or properties that need to be tracking in an application.
- useState accepts an initial state and returns two values:
      - The current state.
      - A function that updates the state.
```js
            import { useState } from "react";
            function FavoriteColor() {
              const [color, setColor] = useState("");
            }
```
# What-is-useEffect?
- The useEffect Hook allows you to perform side effects in your components.
- Some of side effects are: fetching data, directly updating the DOM, and timers.
- useEffect accepts two arguments. The second argument is optional.
      - useEffect(<function>), 
      - useEffect(<dependency>)
- useEffect runs on every render. That means that when the count changes, a render happens,
   which then triggers another effect.
1. No dependency passed:
```js
            useEffect(() => {
              //Runs on every render
            });
```
2. An empty array: Only run the effect on the initial render.
```js
            useEffect(() => {
              //Runs only on the first render
            }, [])
```
3. Props or state values: Here useEffect Hook that is dependent on a variable.
```js
            useEffect(() => {
              //Runs on the first render
              //And any time any dependency value changes
            }, [prop, state]);
```
```js
            import { useState, useEffect } from "react";
            import ReactDOM from "react-dom/client";

            function Timer() {
              const [count, setCount] = useState(0);
              useEffect(() => {
                setTimeout(() => {
                  setCount((count) => count + 1);
                }, 1000);
              });
              return <h1>I've rendered {count} times!</h1>;
            }
```
# What-is-useRef?
- The useRef Hook allows you to persist values between renders.
- If we tried to count how many times our application renders using the useState Hook,
  we would be caught in an infinite loop since this Hook itself causes a re-render.To avoid this, we can use the useRef Hook.
- useRef() only returns one item. It returns an Object called current. When we initialize useRef we set the initial value:    `useRef(0).`
- The useRef Hook can also be used to keep track of `previous state values`. This is because we are able to persist useRef values between renders.


# What-is-useReducer?
- The useReducer Hook is similar to the useState Hook. It allows for custom state logic.
- If you find yourself keeping track of multiple pieces of state that rely on complex logic, useReducer may be useful.
- The useReducer Hook accepts two arguments.
```js
       useReducer(<reducer>, <initialState>)
```
# What-is-useCallback?
- The React useCallback Hook returns a memoized callback function.
- The useCallback Hook only runs when one of its dependencies update.

# What-is-useMemo?
- The React useMemo Hook returns a memoized value.
- Think of memoization as caching a value so that it does not need to be recalculated.
- The useMemo Hook only runs when one of its dependencies update.This can improve performance.

# what-is-difference-between-useCallback-and-useMemo?
- The useMemo and useCallback Hooks are similar. The main difference is that useMemo returns a
  memoized value and useCallback returns a memoized function. 

# What-is-custom-hooks?
- Hooks are reusable functions.
- When you have component logic that needs to be used by multiple components, we can extract that logic to a custom Hook.
- Custom Hooks start with "use". 
```js
Example: useFetch
```























