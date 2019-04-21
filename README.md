# js_notes


## Higher order functions
- returns a function
- put one function into another function
- A good example of a higher order function is filter
    - 
## Callback functions
- functions that you send into another function
- host function will callback to them

## Hoisting
- this is caused because when var is used to declare variables, in the scope it will declare first because it will hoist the variable to the top and do the assignment after
- using let/const instead of var for more predictable behavior 
```js
var text = 'outside';
function logIt(){
    console.log(text);
    var text = 'inside';
};
logIt();
```

```js
var text = 'outside';
function logIt(){
    var text;
    console.log(text);
    text = 'inside';
};
logIt();
```
## Closures
- A feature in JS where the inner function has access to the outer function's variables
- when a function is executed, once it finishes executing it's variables cease to exist
- the inner function preserves the scope chain of the enclosing function at the time the enclosing function was executed, and thus can access the enclosing function’s variables.

## Primitive Data Types
- String, Number, Null, undefined, Boolean, Symbols(ES6)
- When declared and passed as an argument, making changes to the variable that was used as an argument does not persist outside of the function
- When making changes to Objects that were passed as arguments, changes persist

### Using primitive data type
```js
let threatLevel = 1;

function inspireFear(threatLevel){
  threatLevel += 100;
}

inspireFear(threatLevel);
console.log(threatLevel); // Still 1!
```

### Using object
```js
let threatLevel = ['hello', 'world'];

function inspireFear(threatLevel){
  threatLevel.push('!');
  console.log(threatLevel)
}

inspireFear(threatLevel);
console.log(threatLevel); // [ 'hello', 'world', '!' ]
```

## Pass by reference vs Pass by value
- If you pass a variable into a function
  - Pass by reference: if you change the value inside of the function, the change gets reflected tot he variable outside
  - Pass by value: makes a copy and passes into it, changes does not get reflected outside
- JavaScript is all pass by reference
  - When reassigning (using equal) in a function, it will change the address of the location in memory that variable is stored
  - However when you change an object in a function, that change will be reflected since objects can be mutated 
  - Primitive objects cant be mutated, so they are reassigned 
 
### Reassigning primative
```js
let a = 1

let change = (val) => {
  val = 2
}

change(a)
console.log(a) //1
```
- primatives cant be mutated, only reassigned. When you reassign, you change the address

### Reassigning object 
```js
let a = {num: 1}

let change = (val) => {
  val = {}
}
- we are creating a new variable and assigning it to an empty object

change(a)
console.log(a) //{num: 1}
```

### Mutating object
```js
let a = {num: 1}

let change = (val) => {
  val.num = 2
}

change(a)
console.log(a) //{num: 2}
```

## Falsey values 
- False, 0, NaN, undefined, Null, "" (empty string)

## What is node?
- A JavaScript environment that allows you to run/execute a program written in JS
- What makes it good?
    - non-blocking: Think of it as a server loop; going round & round. A request comes in, the loop grabs it and passes it along (like a database query), sets up a callback and repeats. It does not wait for the requested info to come back, instead it goes back into the loop waiting for the next request
    - event driven: Because it is constantly looping, you are not spending anytime waiting for them (return a query). You can have multiple requests opens and will respond to them on their own time.
    - the server only reacts when an event occurs. Could be a request, a file being loaded, or a query being executed
    
## What is express?
- (Simplified) Express.js is to Node.js what Ruby on Rails or Sinatra is to Ruby
- Express is a framework that allows you to organize you web application into an MVC architecture
- Express.js basically helps you manage everything, from routes, to handling requests and views.


## ES6 vs ES5
- 

# Possible interview questions for JS

## var vs let
- var is function scope
- let is block scope
- var gets hoisted

## == vs ===
- both are comparison operators
- == compares value, not type
- === compares value and type

## let vs const
- you can reassign let variables
- const you cannot reassign
- you can modify const if it is not a primitive value
    - you can push to an array, but cant reassign the const to a new array
    
## difference between undefined & null
- both represent empty values
- undefined is the default value when a variable is 
- null is defined by the user
- typeof(undefined) => undefined
- typeof(null) => object

## use of arrow functions?
- when in a function scope, this would refer to the window
    - using fat arrow function will allow for a more predictable output
    
## what is prototypal inheritance?
- every object has a property of prototype where you can add methods and properties to it
- when you create object (b) from object (a), object (b) will inherit all the properties from object (a) through the prototype property
- when you call a method, the object will check itself if it has the method. If not, it will check it's parent to see if the parent has the method. If it does, it will execute the parents method 

## difference between function declaration & function expression
- function expression is an anonymous function saved to a variable
    - will behave like a variable in that it will not exist before it's definition
    - therefore you cannot call it before it's definition
- function declaration is a named function
    - can be called at anytime
```js
function funcD() {
    console.log('I'm a function declaration')
}

let funcE = function() {
    console.log('I'm a function expression')
}
```

## what is a promise? Why do we use it
- is the promise of the eventual completition of something
- Easier to debug/cleaner code

## setTimeout()
- more of a puzzle when asked
- setTimeout() makes it asynchronous making it execute once everything in the call stack has been executed

# General Trivia

## What happens when you go to a url?
1. Type in url
2. Browser looks for IP address
    - Browser cache => OS cache => Router cache => ISP cache => Recursive search
3. Once found, the browser send an HTTP GET request to the web server
4. The webserver responds with a permanent redirect
5. The browser follows the redirect and sends a GET request
6. The server receives the GET request, processes it
7. The server sends back an HTTP response
8. The browser begins rendering the HTML
9. The browser sends reqeuests for objects embedded in HTML and the server sends responses back until page is completed
    - Images, style sheets, javascript
    

