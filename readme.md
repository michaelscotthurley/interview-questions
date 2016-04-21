#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week?
  I learned about how to incorporate an angular app in express.

* What excites or interests you about coding?
  I am excited by the opportunity to improve the lives of people using technolgy,
  by offering visually appealing, effective solutions to daily problems or inconveniences.

* What is a recent technical challenge you experienced and how did you solve it?
*   

* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
*   My primary concern is to build apps with the end user in mind. I believe that all of these disciplines touches the user's experience, albeit in different ways. Security is a primary concern, particularly if apps involve collecting sensitive data. I use technologies such as Bcrypt or Facebook OAuth to handle the hashing of user passwords so that they're never stored in plain text.
*   UI is important, because even the fastest, most efficient application is worthless if user's don't understand how to use it. Therefore I aim for clean, simple designs with clear, concise instructions if needed, and obvious, easy to spot navigation.
*   For performance, technology and maintainability, I take into consideration the size of the application that I am bulding to pick the best tool for the job. I try to keep my code effecient and DRY. Additionally, I comment my code so that another dev can quickly spot code that handles different functionality. I also adhere to standards in naming conventions of files and folders so that my app remains organized. 

* Talk about your preferred development environment.
  I prefer to work in on Apple systems in OS X. My preferred text editor is Sublime Text. As for programming languages, I feel most comfortable working in Javascript or a library such as jQuery. As for full-stack web applications, I find the MEAN stack equal parts challenging and rewarding.

* Which version control systems are you familiar with?
  I am proficient working with Git and Github. I have used both these local and remote tools for version control in both individual and collaborative projects.

* Can you describe your workflow when you create a web page?
  I first define the purpose of the web page or the problem that I am attempting to solve. I then develop user stories that help guide the outline of the core functionality of the site. From there, I wireframe how the site will visually look. After those steps, I decide which technologies I will need to accomplish the completion of the project (i.e. Is this a front-end application or full-stack? Is there an API avilable that could be helpful to populate data for site). I then go about building the "bare bones" of the site. This coudld be as simple as a three file front-end single page website or a fullstack application. From there I go about implementing the wireframed design, seek feedback on usability and adjust as needed.


* If you have 5 different stylesheets, how would you best integrate them into the site?
*   I would combine the stylesheets into one file and uses comments to seperate the different style sheets. 


* Can you describe the difference between progressive enhancement and graceful degradation?
*   Both are approaches to building a website. Progressive enhancement starts with building functionality first for older web browsers and adding functionality that will automatically be enabled by modern browsers. Graceful degradation is a process by which the website is developed with modern browser features in mind, but it also "degrades gracefully" to older browsers so that maximum functionality is maintained. Both approaches should ultimately get to the same result for the end user.


* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).
  I would first create a bare bones HTML site in which I would create a div element with a particular class or ID. Then I would use CSS to style the div to meet the alignment and size specifications that I desired. Then, I would write a javascript applicaiton to manipulate this DOM element to cycle through images.


* If you could master one technology this year, what would it be?
  ReactJS

* Explain the importance of standards and standards bodies.
  Standards and the bodies that create them, are imprortant to the advancement of the web development. Without standards, it would be difficult to develop applications that were supported by all commonly used web browsers. Standards ensure that code will work for the user, regardless of OS or browser selection.


## HTML Questions

* What does a `doctype` do?
*   It instructs the web browser about which version the markup language is written in.
* What's the difference between HTML and XHTML?
*   XHTML is essentially vanilla HTML expressed as XML. XHTML is a stricter version of HTML and helps developers from writing "bad" html that does not correctly render on a user's device.
* What are `data-` attributes good for?
*   Data attributes are good for creating a class of attributes for a particular element in the DOM. These attributes can then be defined and manipulted using scripts.
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
* Cookies are stored on the client's computer and persist (unless deleted by the user). They are often used as a means to help speed up authentication for user's on return visits to sites. Local storage is stored on the client side, but only persists while the user's window is open. Session storage is similar to local storage only the storage is handled on the server side.
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
*   As the browser renders elements sequentially as the page loads, it is best practice to place the link references in the head so that they inform the browser to load the correct styling as the page loads. If you have custom style sheets, they should be listed after any framework stylesheets such as Bootstrap. Scripts should be loaded just before the closing body tag so as not to interupt the page from loading it's content while attempting to download and execute a script.

## CSS Questions

* What is the difference between classes and IDs in CSS?
  IDs are unique to one element and are defined in css with the # symbol. Classes apply to any elements to which they are assigned and are prefixed with a "." in css files.

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
*   Resetting CSS simply involves removing all default styling of all elements on the page. Normalizing aims to make the standard elements (i.e. h1-h6, p, strong) appear the same accross all browsers. I would chose normalize as it would require only minor tweeks to the stylesheet to modify elements. It would also ensure that the page would look good across different browers.
* Describe Floats and how they work.
*   The float CSS property specifies that an element should be taken from the normal flow and placed along the left or right side of its container, where text and inline elements will wrap around it.
* Describe z-index and how stacking context is formed.
* The z-index property in CSS controls the vertical stacking order of elements that overlap. As in, which one appears as if it is physically closer to you. z-index only effects elements that have a position value other than static (the default).
* Have you ever used a grid system, and if so, what do you prefer?
* I have used both Materialize and Bootstrap. I love Bootstrap for it's cleanliness and simplicity.
* Have you used or implemented media queries or mobile specific layouts/CSS?
*   Yes I implement media queries routinely in my projects to aid in making my pages more responsive. My Seattle Showdown app removes overlayed title text when the the window size is at or below 700px. This prevents the absolutely positined text from running over it's intended space.
* How do you optimize your webpages for print?
*   Using simple color combinations with good contrast.
* What are the advantages/disadvantages of using CSS preprocessors?
*   
  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
* Explain how a browser determines what elements match a CSS selector.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
* List as many values for the display property that you can remember.
* What's the difference between inline and inline-block?
* What's the difference between a relative, fixed, absolute and statically positioned element?
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* Have you played around with the new CSS Flexbox or Grid specs?
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* Explain some of the pros and cons for CSS animations versus JavaScript animations.

## JS Questions

* Explain event delegation
* Explain how `this` works in JavaScript
* Explain how prototypal inheritance works
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?
  * How would you go about checking for any of these states?
* What is a closure, and how/why would you use one?
* What's a typical use case for anonymous functions?
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
* What's the difference between `.call` and `.apply`?
* Explain `Function.prototype.bind`.
* What's the difference between feature detection, feature inference, and using the User Agent string?
* Explain AJAX in as much detail as possible.
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
* Explain "hoisting".
* Describe event bubbling.
* What's the difference between an "attribute" and a "property"?
* Why is extending built-in JavaScript objects not a good idea?
* What is the difference between `==` and `===`?
* Explain the same-origin policy with regards to JavaScript.
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
* What tools and techniques do you use debugging Javascript code?
* What language constructions do you use for iterating over object properties and array items?

## Database Questions

* Design a database schema for Facebook, with at least 4 models, a complete set of attributes for each model, a 1:M association, and a M:M association.

## Ruby/Rails
* What are ruby gems?
* What is the difference between a symbol and a string?
* What is the difference between a class method and an instance method?
* What is the difference between local variables, instance variables, and class variables?
* What is a range?
* In ruby, what does attr_accessor do?  
* What is the purpose of environment files under the config folder in Rails? (development, test, production)
* What is the purpose of the application.rb file in Rails?
* How can you define a constant?
* What is the purpose of `yield`?
* How do you store API keys when creating an app?
* How do I send parameters through a url?
* Explain MVC
* What is a `before_action`? When would you use it?
* What do controllers do in rails?
* What is RESTful routing?
* What is a polymorphic association?
* What are params?
* How do I make a migration to add a column in Rails?
* What is CSRF? How does Rails protect an app against this?
* What's the difference between `User.find_by_id(1)` and `User.find(1)`?
* What's are classes in Ruby? What are modules? And what's the difference?

## Testing Questions

* What are some advantages/disadvantages to testing your code?
* What tools would you use to test your code's functionality?
* What is the difference between a unit test and a functional/integration test?
* What is the purpose of a code style linting tool?
* What is End-to-end (E2E) testing? How can it be implemented in frameworks like Angular and Rails?

## Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```

## Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Do you have any pet projects? What kind?
* How do you like your coffee?
