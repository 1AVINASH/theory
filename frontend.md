## Webpack
* Module bundler for js applications
* Takes application's modules (js files, css, images, etc) and their dependencies and bundles them into static assets that can be used in a web browser



## Functions vs Const

## Closure

## DOM

## Promise
* In JavaScript, a Promise is an object that represents the eventual completion (or failure) of an asynchronous operation and its resulting value. It acts as a placeholder for a value that is not yet available but will be at some point in the future. 
Promises are used to manage asynchronous code more effectively, offering a cleaner and more readable alternative to traditional callback functions, which can lead to "callback hell" in complex scenarios.

## Side Effect
* It refers to any operation which has any effect outside the component's immediate rendering logic and its internal state/props. Essentially, it's anything that can cause an observable change outside the component
* Common examples of side effects
    * Making async requests to an API or server
    * Manipulaing the document object model directly (like changing the page title, adding or removing classes, or manipulating elements outisde of React's virtual DOM)
    * Using setTimeout or setInterval
    * Interacting with browser APIs like localStorage, sessionStorage, etc.
* They are called side effects because unlike normal functions that behave predictively, these functions can modify values outside their scope, thus introducing an element of unpredictability.
* In react, useEffect hook can be used for managing side effects

## == vs ===
* In JavaScript, == (loose equality) and === (strict equality) are both used for comparison, but they differ in how they handle type coercion:
* == (Loose Equality): This operator performs type coercion before comparing the values. If the operands are of different data types, JavaScript will attempt to convert one or both operands to a common type before making the comparison. This can lead to unexpected results if you are not aware of the implicit type conversions.
* === (Strict Equality): This operator compares both the value and the data type of the operands without performing any type coercion. If the operands are of different data types, the comparison will immediately return false, regardless of their values. This provides a more predictable and robust comparison.

## React Methods
### UseRef
### UseEffect
* Used to perform methods whenever an object's value changes
* In the return method of such components, you can define functions which will be used as destructors for this method
* Primarily used for managing side effects in functional components. Side effects include data fetching, subscriptions, manual DOM manipulations, and setting up event listeners

### UseState

### UseCallback
* React Hook that memoizes a function definition, preventing its re-creation on every render of a component, unless its dependencies change. This is a performance optimization technique primarily used in scenarios where referential equality of functions is important,
* useCallback takes two arguments:
    * The function to memoize: This is the callback function you want to prevent from being recreated on every render.
    * A dependency array: This array contains values (props, state, or other variables) that the memoized function depends on. The function will only be re-created if any of these dependencies change.
* ```
import React, { useState, useCallback } from 'react';

function ParentComponent() {
  const [count, setCount] = useState(0);

  // Without useCallback, this function would be recreated on every render
  // const handleClick = () => {
  //   setCount(prevCount => prevCount + 1);
  // };

  // With useCallback, this function is only recreated when 'count' changes
  const handleClick = useCallback(() => {
    setCount(prevCount => prevCount + 1);
  }, []); // Empty dependency array means it's created once and never changes

  return (
    <div>
      <p>Count: {count}</p>
      <ChildComponent onClick={handleClick} />
    </div>
  );
}


```
### UseCallback vs UseEffect
* The callback function passed to useEffect runs after every render where its dependencies have changed. It can also run on component mount and cleanup on unmount.
* UseCallback prevents re-rendering of function even on component re-renders unless something in the dependency array is changed


### Round vs Curly Brackets in JS
* Round brackets are primarily used for control flow, function-related operations, and grouping expressions.
* Curly brackets are primarily used for defining blocks of code, creating objects, and destructuring.
* Curly brackets are also used for jsx expressions, i.e., embedding javascript expressions within the HTML-like structure
* Usually curly brackets can be used for destructuring but for destructuring arrays, square brackets are used

### DOM (Document Object Model)
* Programming interface for documents, specifically HTML and XML. 
* Represents the structure if a dicynebt as a tree of objects allowing programming languages like Javascript to interact with and modify the content, structure, and style of a web page dynamically
* It organizes the elements of an HTML or XML document in a hierarchical, tree like structure. Each element, attribute, and piece of text in the document is represented as a "node" within this tree
* Each node in the DOM tree is an object, meaning it has properties and methods
---

* All the divs and html is rendered first, and the hooks are triggered once they are completed


