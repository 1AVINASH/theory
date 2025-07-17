## Webpack
* Module bundler for js applications
* Takes application's modules (js files, css, images, etc) and their dependencies and bundles them into static assets that can be used in a web browser



## Functions vs Const

## Closure

## DOM

## Promise
* In JavaScript, a Promise is an object that represents the eventual completion (or failure) of an asynchronous operation and its resulting value. It acts as a placeholder for a value that is not yet available but will be at some point in the future. 
Promises are used to manage asynchronous code more effectively, offering a cleaner and more readable alternative to traditional callback functions, which can lead to "callback hell" in complex scenarios.


## == vs ===
* In JavaScript, == (loose equality) and === (strict equality) are both used for comparison, but they differ in how they handle type coercion:
* == (Loose Equality): This operator performs type coercion before comparing the values. If the operands are of different data types, JavaScript will attempt to convert one or both operands to a common type before making the comparison. This can lead to unexpected results if you are not aware of the implicit type conversions.
* === (Strict Equality): This operator compares both the value and the data type of the operands without performing any type coercion. If the operands are of different data types, the comparison will immediately return false, regardless of their values. This provides a more predictable and robust comparison.

## React Methods
### UseRef
### UseEffect
* Used to perform methods whenever an object's value changes
* In the return method of such components, you can define functions which will be used as destructors for this method

### UseState


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


