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
In the example above, ### getElementById is a method, while innerHTML is a property.
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
