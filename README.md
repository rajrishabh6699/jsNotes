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

The HTML elements as objects
The properties of all HTML elements
The methods to access all HTML elements
The events for all HTML elements
A property is a value that you can get or set (like changing the content of an HTML element).
A method is an action you can do (like add or deleting an HTML element).

```<html>
<body>
<p id="demo"></p>
<script>
document.getElementById("demo").innerHTML = "Hello World!";
</script>

</body>
</html>
```
In the example above, ### getElementById is a method, while innerHTML is a property.
The innerHTML property can be used to get or change any HTML element, including <html>
and <body>.
  
### **Methods**
document.getElementById(id): Find an element by element id
document.getElementsByTagName(name): Find elements by tag name
document.getElementsByClassName(name): Find elements by class name
document.querySelector() : Returns the first element that matches a specified CSS selector(s) in the document.
document.querySelectorAll() : Returns all elements in the document that matches a specified CSS selector(s), as a static NodeList object.

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

In order to listen to multiple buttons or elements we use querySelectorALL()
In order to attach event handler to all the elements or buttons we need to loop them using
foreach()
eg.
- buttons.forEach(function(button) { //button is just a parameter to traverse all the
//elements in buttons
- Console.log(‘hey’);
- buttons.addEventListener(‘click’, function { console.log(‘hey again’) //this anonymous
//function is known as

//event handler
- });

Target property tells that which element has triggered the event.
Target (the event which is being fired) and currentTarget(the main element) difference :
target is the element that triggered the event (e.g., the user clicked on) currentTarget is the
element that the event listener is attached to
Why event.target === event.currentTarget are same not always only when there are no other
tags attached.
**Propagation**: Flow to events getting triggered
**Event bubbling** : events get triggered from child to parents from bottom to up
There are two ways of event propagation in the HTML DOM, bubbling and capturing.
Event propagation is a way of defining the element order when an event occurs. If you have a
<p> element inside a <div> element, and the user clicks on the <p> element, which element's
"click" event should be handled first?
In bubbling the inner most element's event is handled first and then the outer: the <p> element's
click event is handled first, then the <div> element's click event.
We can stop bubbling by using stopPropagation() function

**Event capture**: goes from the root of the DOM tree to way down till the target node.
Eg:
- window.addEventListener
- (
- ‘click’, function(event)
- { console.log(‘you clicked the window’)
- },
- {capture:true}
- );
Console.log(e.currentTarget) and console.log(this) to get the current node but this keyword has
a downside with the arrow function related to its scope. Recommended to not use this in
eventListener’s callback function ??
- //confirm
- //Prompt
- //console.dir(event.target)
- //includes
Events :
- //keyup
- //keydown
- //focus
- //blur
- //event.key
**event.PreventDefault()**
## Module-7
* B brackets
* E exponents
* D ivision

* M ultiplication
* A ddition
* S ubration
- //.replace(/\s/g,’-‘) //regex-regular expression
- //console.group()
- //console.groupend()
Empty string is not true it is not false its an empty string
**Truthy**: which are equated to true I.e. all numbers and any value , empty array and empt
object also.
**Falsey** : which equates to false eg : 0 for numbers and empty string for strings. , undefined ,
null , NaN
**Coercion** converting something of a different datatype into another type
And ! Operator coerces any datatype into a true boolean(either true or false).
**Shortcircuiting** (with if condition and &&) and its solution:
Use a single &. That is a bitwise operator. It will execute all conditions and then return a bitwise
sum of the results.
- function checkAll() {
- return checkSomething(1)
- & checkSomething(2)
- & checkSomething(3)
- }

The window object allows execution of code at specified time intervals.
These time intervals are called timing events.
The two key methods to use with JavaScript are:
**1. setTimeout(function, milliseconds)** :Executes a function, after waiting a specified number
of milliseconds.
**2. setInterval(function, milliseconds)** :Same as setTimeout(), but repeats the execution of the
function continuously. Will not run immediately so you have to make your own immediate
function by calling the call_back function immediately inside your customised function.
**3. clearTimeout(reference to the setTimeout function i.e in a variable)**:for stoping
setTimeout.
How to stop an interval after x seconds:
- setTimeout(function() {
- clearInterval( reference var name) } , 3000);

**Map**:
Const myMap=new Map( )
.set( )
.has( )
.delete( )
Key can be of any type.
Array methods : * .length( )
* .slice( )
* .push( ) //Add to the end
* .unshift( ) // Add to the front of the array
* .shift( ) // remove first item
If you do not want to change the original array because of mutation methods use the copy of the
array by spreading the array.
Static methods on arrays:
* Array.of( )
* Array.from( )
* Array.isArray( )
Static methods on objects:
* Object.entries( ): return Array of keys and values e.g. [keys, values]
* Object.keys( ) : return Array of keys e.g. [keys]
* Object.values( ) : return Array of values e.g. [values
// indexOf( )
//lastIndexOf( )

## Module-11
**New keyword**: When used along with any data type makes an object out of it.
When we use new keyword on a function it creates an instance object of that function instead of
what has been returned from that function.
E.g. function pizza {
return console.log(‘hey’)
}
const pizza2= new Pizza( ); //this is an instance of pizza function . This
//will not return what pizza returns.
**This keyword**: this keyword is bound to the current object or instance of the object.It stores
the data and have functionalities over the properties of the object.
**Prototype function**: object.prototype.function_name= function ( ) {
//write your code here
}
**Bind call and apply** : functions those changes the scope of “this” keyword inside of a

method.
E.g screenshot
**Call**: it will return as well as bind the function at that time only.
**Apply**: accepts single array of arguments along with the this object.
## Module -12
Javascript is a single threaded language.
Javascript is asynchronous means it does not stop.

**Callback Hell**:Callback hell is caused by poor coding practices.Asynchronous JavaScript, or
JavaScript that uses callbacks, is hard to get right intuitively. A lot of code cluters and there are
so many this , then functions to deal with.
**Promises**:Promises are a way to write async code that still appears as though it is executing
in a top-down way, and handles more types of errors due to encouraged use of try/catch style
error handling.A JavaScript Promise object can be:
* Pending
* Fulfilled
* Rejected
The Promise object supports two properties: state and result.
While a Promise object is "pending" (working), the result is undefined.
When a Promise object is "fulfilled", the result is a value.
When a Promise object is "rejected", the result is an error object.
**How to write a Promise**:
function myDisplayer(some) {
document.getElementById("demo").innerHTML = some;
}
let myPromise = new Promise(function(myResolve, myReject) {
let x = 0;
// The producing code (this may take some time)
if (x == 0) {
myResolve("OK");
} else {
myReject("Error");
}
});
myPromise.then(
function(value) { /* code if successful */ },
function(error) { /* code if some error */ }
);

**Async/Await**:There’s a special syntax to work with promises in a more comfortable fashion,
called “async/await”.
The **async** keyword can be placed before a function, like this:
async function f() {

return 1;
}
The word “async” before a function means one simple thing: a function always returns a
promise. Other values are wrapped in a resolved promise automatically.So, async ensures that
the function returns a promise, and wraps non-promises in it. There’s another keyword,
**await**, that works only inside async functions.The keyword await makes JavaScript wait until
that promise settles and returns its result.
// works only inside async functions
let value = await promise;
async function f() {
let promise = new Promise((resolve, reject) => {
setTimeout(() => resolve("done!"), 1000)
});
let result = await promise; // wait until the promise resolves (*)
alert(result); // "done!"
}
f();
Await literally suspends the function execution until the promise settles, and then resumes it
with the promise result. That doesn’t cost any CPU resources, because the JavaScript engine
can do other jobs in the meantime: execute other scripts, handle events, etc.
It’s just a more elegant syntax of getting the promise result than promise.then. And, it’s easier to
read and write.
### API
An API is generally a set of code features (e.g. methods, properties, events, and URLs) that a
developer can use in their apps for interacting with components of a user's web browser, or
other software/hardware on the user's computer, or third party websites and services.
Methods are :
**fetch()**:The Fetch API provides a fetch() method defined on the window object. It also
provides a JavaScript interface for accessing and manipulating parts of the HTTP pipeline
(requests and responses). The fetch method has one mandatory argument- the URL of the
resource to be fetched. This method returns a Promise that can be used to retrieve the
response of the request.
**Axios.js**: Axios is a Javascript library used to make HTTP requests from the browser and it
supports the Promise API
Axios performs automatic transforms of JSON data.
Fetch is a two-step process when handling JSON data- first, to make the actual request;
second, to call the .json() method on the response.
* To get the json object response: in fetch call the json() function on the response object, in
Axios get data property of the response object.
Axios allows cancelling request and request timeout.
Fetch does not.
Fetch act on body and axis act on data.
* Fetch has no url in request object, Axios has url in request object

* Fetch request function includes the url as parameter, Axios request function does not include
the url as parameter.
