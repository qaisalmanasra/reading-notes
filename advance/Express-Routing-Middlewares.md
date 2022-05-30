# **Express REST API**
>## ***Classes***
#### Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics.
## **`Defining classes`**
### `Class declarations`
```
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}
```
### `Hoisting`
#### Functions can be called in code that appears before they are defined, classes must be defined before they can be constructed. 
### `Class expressions`
A class expression is another way to define a class. Class expressions can be named or unnamed.
```
// unnamed
let Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
console.log(Rectangle.name);
// output: "Rectangle"

// named
let Rectangle = class Rectangle2 {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
console.log(Rectangle.name);
// output: "Rectangle2"
```
## **`Class body and method definitions`**
### - `Strict mode`
### - `Constructor`
### - `Static initialization blocks`
### - `Prototype methods`
### - `Generator methods`
### - `Static methods and properties`

## **`Sub classing with extends`**
#### The extends keyword is used in class declarations or class expressions to create a class as a child of another class.
#### If there is a constructor present in the subclass, it needs to first call super() before using "this".
#### Note that classes cannot extend regular (non-constructible) objects. If you want to inherit from a regular object, you can instead use Object.setPrototypeOf()
## **`Species`**
#### You might want to return Array objects in your derived array class MyArray. The species pattern lets you override default constructors.

#### For example, when using methods such as map() that returns the default constructor, you want these methods to return a parent Array object, instead of the MyArray object. The Symbol.species symbol lets you do this:
```
class MyArray extends Array {
  // Overwrite species to the parent Array constructor
  static get [Symbol.species]() { return Array; }
}

let a = new MyArray(1,2,3);
let mapped = a.map(x => x * x);

console.log(mapped instanceof MyArray); // false
console.log(mapped instanceof Array);   // true
```
### **[Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)**
***
>## ***Routing***
Routing refers to how an application’s endpoints (URIs) respond to client requests.
## **`Route methods`**
A route method is derived from one of the HTTP methods, and is attached to an instance of the express class.
#### Express supports methods that correspond to all HTTP request methods: get, post, and so on.
## **`Route paths`**
#### Route paths, in combination with a request method, define the endpoints at which requests can be made. Route paths can be strings, string patterns, or regular expressions.
## **`Route handlers`**
#### You can provide multiple callback functions that behave like middleware to handle a request. The only exception is that these callbacks might invoke next('route') to bypass the remaining route callbacks. You can use this mechanism to impose pre-conditions on a route, then pass control to subsequent routes if there’s no reason to proceed with the current route.
## **`app.route()`**
#### You can create chainable route handlers for a route path by using app.route(). Because the path is specified at a single location, creating modular routes is helpful, as is reducing redundancy and typos
## **`Conclusion`**
* #### Use express.Router() multiple times to define groups of routes
* #### Apply the express.Router() to a section of our site using app.use()
* #### Use route middleware to process requests
* #### Use route middleware to validate parameters using .param()
* #### Use app.route() as a shortcut to the Router to define multiple requests on a route
### **[Reference1](https://expressjs.com/en/guide/routing.html)**
### **[Reference2](https://www.digitalocean.com/community/tutorials/learn-to-use-the-new-router-in-expressjs-4)**
*** 