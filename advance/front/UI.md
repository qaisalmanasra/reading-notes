# Component Based UI
## React Hello World
***
#### The smallest React example looks like this:
```
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<h1>Hello, world!</h1>);
```
## Introducing JSX
### Why JSX?
#### React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.

#### Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both. We will come back to components in a further section, but if you’re not yet comfortable putting markup in JS, this talk might convince you otherwise.

#### React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React to show more useful error and warning messages.

### Embedding Expressions in JSX
#### You can put any valid JavaScript expression inside the curly braces in JSX. For example, 2 + 2, user.firstName, or formatName(user) are all valid JavaScript expressions.
#### We split JSX over multiple lines for readability. While it isn’t required, when doing this, we also recommend wrapping it in parentheses to avoid the pitfalls of automatic semicolon insertion.

### JSX is an Expression Too
#### After compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.

#### This means that you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions

### Specifying Attributes with JSX

* #### You may use quotes to specify string literals as attributes.
* #### You may also use curly braces to embed a JavaScript expression in an attribute.
* #### Don’t put quotes around curly braces when embedding a JavaScript expression in an attribute. You should either use quotes (for string values) or curly braces (for expressions), but not both in the same attribute.
```
Warning:

Since JSX is closer to JavaScript than to HTML, React DOM uses camelCase property naming convention instead of HTML attribute names.

For example, class becomes className in JSX, and tabindex becomes tabIndex.
```
### Specifying Children with JSX
* #### If a tag is empty, you may close it immediately with />, like XML.

* #### JSX tags may contain children.

### SX Prevents Injection Attacks
* #### It is safe to embed user input in JSX:

* #### By default, React DOM escapes any values embedded in JSX before rendering them. Thus it ensures that you can never inject anything that’s not explicitly written in your application. Everything is converted to a string before being rendered. This helps prevent XSS (cross-site-scripting) attacks.
## Rendering Elements
##### Elements are the smallest building blocks of React apps.

* #### An element describes what you want to see on the screen.
* #### Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.

### [react hello world](https://reactjs.org/docs/hello-world.html)
### [introducing JSX](https://reactjs.org/docs/introducing-jsx.html)
### [rendering elements](https://reactjs.org/docs/rendering-elements.html)
### [sass cheatsheet](https://devhints.io/sass)
### [react cheatsheet](https://devhints.io/react)
### [react cheatsheet2](https://reactcheatsheet.com/)

