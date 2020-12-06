<h1>JavaScript-DOM-manipulation</h1>
<h3>Get to know the web browser</h3>

But before going to touch the DOM, we should have an overview of a web browser.

<img src="https://miro.medium.com/max/664/1*g74TsQozyLHtvqwCK18hNA.png" alt=""/>

<ul>
<li>
<strong>The Navigator</strong>
represents the state and identity of the browser, which is in JavaScript represented by the
<code>Navigator</code> 
object. We can use this object to retrieve things like the user-agent, 
user’s settings or access user’s computer hardware i.e. webcam etc.
</li>
<li>
<strong>The Window</strong> 
is the browser tab that a web page is loaded into,
which is represented by the 
<code>Window</code> object in JavaScript. We can do many things with this object such as get the current width/height of the
window, access user’s storage or attach an event handler…
</li>
<li>The <strong>Document</strong> is the actual page loaded into the window, and is represented in JavaScript by the 
<code>Document</code> object. This is also as known as DOM, the super star in the web development. 
Most of the modifications we made to the web is by manipulating the document. So, 
this is the main focus of this article.
</li>
</ul>

<h2>The Document Object Model (DOM)</h2>

The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects. That way, programming languages can connect to the page.

Basically, when a browser loads a page it creates an object model of that page and prints it on the screen. The object model is represented in a tree data structure, each node is an object with properties and methods, and the topmost node is the document object.

A programming language can be used to access and modify this object model, and this action is called DOM manipulation. And we will do that with JavaScript.

```
<!-- Index.html file -->
<html>
  <head>
    <title> DOM Manipulation </title>
  </head>
  <body>
    <div id="division"> <h1 id="head"> <em>DOM <em> manipulation </h1>
      <p class="text" id="middle">Tutorial </p> <p>Sibling </p>
      <p class="text" > Medium Tutorial </p>
    </div >
    <p class="text" > Out of the div </p>
    <!-- Then we call the javascript file -->
    <script src="manipulation.js"> </script>
  </body>
</html>
```

<h4>Accessing the elements or single element</h4>

<pre>
// the method below selects the element with the id ofhead
let id = document.getElementById('head');

// the code below selects the first p element inside the first div
let q = document.querySelector('div p');

/* Extra code */
// this changes the color to red
id.style.color = 'red';

// give a font size of 30px
q.style.fontSize = '30px';
</pre>

