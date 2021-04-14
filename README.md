# **JAVASCRIPT HISTORY**
JavaScript is everywhere, and for the seventh year in a row, it has been ranked the most commonly used programming language, with 67.8% of developers employing it in 2019. Its ascent to the world’s most popular programming language is synonymous with the rise of the internet itself.

Created out of necessity, it is used to build 95.2% (1.52 billion) of websites today, including some of the world’s largest, like Facebook and YouTube. Without it, we would not have popular and useful web apps such as Google Maps and eBay. 

The early to mid-1990s was an important time for the internet. Key players like Netscape and Microsoft were in the midst of browser wars, with Netscape’s Navigator and Microsoft’s Internet Explorer going head to head.

In September 1995, a Netscape programmer named Brandan Eich developed a new scripting language in just 10 days. It was originally named Mocha, but quickly became known as LiveScript and, later, JavaScript.

# **DATATYPES IN JS**
JavaScript variables can hold many data types:
* String
* Number
* Object
* Boolean
* Null
* Undefined
* Symbol

### **Strings**
A JavaScript string is zero or more characters written inside quotes.

### **Numbers**
JavaScript has only one type of number. Numbers can be written with or without decimals.

### **Objects**
A JavaScript object has properties associated with it. A property of an object can be explained as a variable that is attached to the object. Object properties are basically the same as ordinary JavaScript variables, except for the attachment to objects.

### **Boolean**
A JavaScript Boolean represents one of two values: true or false.

### **Null**
In JavaScript null is "nothing". It is supposed to be something that doesn't exist.
Unfortunately, in JavaScript, the data type of null is an object.

### **Undefined**
In JavaScript, a variable without a value, has the value undefined. The type is also undefined.

# **FUNCTIONS IN JS**
A JavaScript function is a block of code designed to perform a particular task.
A JavaScript function is executed when "something" invokes it (calls it).

```javascript
function demoFunc() {
  console.log("Hello World");
}
```

# **Closures**
A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function’s scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.



# **DOM Manipulation**
When writing web pages and apps, one of the most common things you'll want to do is manipulate the document structure in some way. This is usually done by using the Document Object Model (DOM), a set of APIs for controlling HTML and styling information that makes heavy use of the Document object.
When a web page is loaded, the browser creates a Document Object Model of the page.

The HTML DOM model is constructed as a tree of Objects.The HTML DOM is a standard object model and programming interface for HTML. It defines:

* The HTML elements as objects
* The properties of all HTML elements
* The methods to access all HTML elements
* The events for all HTML elements
* A property is a value that you can get or set (like changing the content of an HTML element).
* A method is an action you can do (like add or deleting an HTML element).

```<html>
<body>
<p id="demo"></p>
<script>
document.getElementById("demo").innerHTML = "Hello World!";
</script>

</body>
</html>
```
In the example above, getElementById is a method, while innerHTML is a property.
The innerHTML property can be used to get or change any HTML element, including <html>
and <body>.
  
### **Methods**
* document.getElementById(id): Find an element by element id
* document.getElementsByTagName(name): Find elements by tag name
* document.getElementsByClassName(name): Find elements by class name
* document.querySelector() : Returns the first element that matches a specified CSS selector(s) in the document.
* document.querySelectorAll() : Returns all elements in the document that matches a specified CSS selector(s), as a static NodeList object.

# **Event Listeners**
The EventListener interface represents an object that can handle an event dispatched by an EventTarget object.
Event listeners are among the most frequently used JavaScript structures in web design. 
They allow us to add interactive functionality to HTML elements by “listening” to different events that
take place on the page, such as when the user clicks a button, presses a key, or when an
element loads.
```
const myButton = document.querySelector(‘.submitButton’); //get the first element of the class using querySelector
myButton.addEventListener(‘click’, ()=>{
    console.log("Hey! You Clicked Me");
})
```

### **Bubbling**
The bubbling principle is simple.
When an event happens on an element, it first runs the handlers on it, then on its parent, then all the way up on other ancestors.
Let’s say we have 3 nested elements FORM > DIV > P with a handler on each of them:

```
<style>
  body * {
    margin: 10px;
    border: 1px solid blue;
  }
</style>

<form onclick="alert('form')">FORM
  <div onclick="alert('div')">DIV
    <p onclick="alert('p')">P</p>
  </div>
</form>
```

A click on the inner `<p>` first runs onclick: 
* On that `<p>`
* Then on the outer `<div>`
* Then on the outer `<form>`
* And so on upwards till the document object

### **Capturing**
There’s another phase of event processing called “capturing”. It is rarely used in real code, but sometimes can be useful.
The standard DOM Events describes 3 phases of event propagation:

* Capturing phase-the event goes down to the element.
* Target phase-the event reached the target element.
* Bubbling phase-the event bubbles up from the element.

###### **For more information visit** 
https://javascript.info/bubbling-and-capturing 

# **Getting Loopy**
Loops offer a quick and easy way to do something repeatedly.
```
for (let step = 0; step < 5; step++) {
  // Runs 5 times, with values of step 0 through 4.
  console.log('Walking east one step');
}
```

### **For Loop**
A for loop repeats until a specified condition evaluates to false. The JavaScript for loop is similar to the Java and C for loop.
A for statement looks as follows:
```
for ([initialExpression]; [conditionExpression]; [incrementExpression])
  statement
```
### **For In Loop**
The for...in statement iterates a specified variable over all the enumerable properties of an object. For each distinct property, JavaScript executes the specified statements.

### **For Of Loop**
The for...of statement creates a loop Iterating over iterable objects (including Array, Map, Set, arguments object and so on), invoking a custom iteration hook with statements to be executed for the value of each distinct property.

### **While Loop**
A while statement executes its statements as long as a specified condition evaluates to true. A while statement looks as follows:
```
while (condition)
  statement
```
If the condition becomes false, statement within the loop stops executing and control passes to the statement following the loop.

The condition test occurs before statement in the loop is executed. If the condition returns true, statement is executed and the condition is tested again. If the condition returns false, execution stops, and control is passed to the statement following while.

To execute multiple statements, use a block statement ({ ... }) to group those statements.

### **For Each**
The forEach() method executes a provided function once for each array element.
```
const array1 = ['a', 'b', 'c'];

array1.forEach(element => console.log(element));

// expected output: "a"
// expected output: "b"
// expected output: "c"
```
### **Map**
The map() method creates a new array with the results of calling a function for every array element.
The map() method calls the provided function once for each element in an array, in order.
```
array.map(function(currentValue, index, arr), thisValue)
```

### **Reduce**
The reduce() method reduces the array to a single value.
The reduce() method executes a provided function for each value of the array (from left-to-right).
The return value of the function is stored in an accumulator (result/total).
```
array.reduce(function(total, currentValue, currentIndex, arr), initialValue)
```

# **Advanced Flow Control**
* JS is asynchronous.
* Different languages are there which are multithreaded, but JS is single threaded i.e. only one thing can only be run at a time.
* If we want to do one thing after another, we must nest the callbacks inside each other (this is called Callback Hell), because they all depend upon the previous callbacks in order to maintain the order.

The solution to this problem of Callback hell is Promises.

### **Promises**
* Whenever we are not getting immediate data return, we can use Promises to get a promise instead, that like eventually after sometime I will get some data back.
* Promises are made immediately but they are not resolved or rejected immediately.
* We use .then() to access the resolved value. Whenever we want to perform series of operations we can chain multiple results.
* In order to catch error in promise we chain a .catch().
* If we have multiple promises sequentially placed by .then() chaining we dont have to put explicit .catch() for each of them, only a single .catch() in the end would do. But in this case all the others after the breakpoint will get rejected. For resolving this problem, we use promise.allSettled()
* Promise.all() assumes that all of them go successfully and if we want to catch the error we would have to specify the catch block.

*Promises are great but syntax is again similar to the callbacks used earlier. We are still inside one level of callback.*

**Async/Await is a new syntax for neat looking code.**
The functions that returns promises still stay exactly the same way, nothing changes in promise generating fucntions, its all in where we actually call the code where Async/Await comes in handy.
An async function is a function declared with the async keyword, and the await keyword is permitted within them. The async and await keywords enable asynchronous, promise-based behavior to be written in a cleaner style, avoiding the need to explicitly configure promise chains.
```
function resolveAfter2Seconds() {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve('resolved');
    }, 2000);
  });
}

async function asyncCall() {
  console.log('calling');
  const result = await resolveAfter2Seconds();
  console.log(result);
  // expected output: "resolved"
}

asyncCall();
```

# **API**
* API stands for Application Programming Interface.
* A Web API is an application programming interface for the Web.
* A Browser API can extend the functionality of a web browser.
* A Server API can extend the functionality of a web server.

# **CORS**
Cross-Origin Resource Sharing (CORS) is an HTTP-header based mechanism that allows a server to indicate any other origins (domain, scheme, or port) than its own from which a browser should permit loading of resources. CORS also relies on a mechanism by which browsers make a “preflight” request to the server hosting the cross-origin resource, in order to check that the server will permit the actual request. In that preflight, the browser sends headers that indicate the HTTP method and headers that will be used in the actual request.

# **Modules**
As our program grows bigger, it may contain many lines of code. Instead of putting everything in a single file, you can use modules to separate codes in separate files as per their functionality. This makes our code organized and easier to maintain.
Module is a file that contains code to perform a specific task. A module may contain variables, functions, classes etc.

Suppose, a file named greet.js contains the following code:

```
// exporting a function
export function greetPerson(name) {
    return `Hello ${name}`;
}
```
Now, to use the code of greet.js in another file, you can use the following code:
```
// importing greetPerson from greet.js file
import { greetPerson } from './greet.js';

// using greetPerson() defined in greet.js
let displayName = greetPerson('Jack');

console.log(displayName); // Hello Jack
```





