# Front-end Job Interview Questions

This file contains a number of front-end interview questions that can be used when vetting potential candidates. It is by no means recommended to use every single question here on the same candidate (that would take hours). Choosing a few items from this list should help you vet the intended skills you require.

**Note:** Keep in mind that many of these questions are open-ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would.

## Table of Contents

  1. [General Questions](#general-questions)
  1. [HTML Questions](#html-questions)
  1. [CSS Questions](#css-questions)
  1. [JS Questions](#js-questions)
  1. [Testing Questions](#testing-questions)
  1. [Performance Questions](#performance-questions)
  1. [Network Questions](#network-questions)
  1. [Coding Questions](#coding-questions)
  1. [Fun Questions](#fun-questions)

## Getting Involved

  1. [Contributors](#contributors)
  1. [How to Contribute](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/CONTRIBUTING.md)
  1. [License](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/LICENSE.md)

#### General Questions:

* What did you learn yesterday/this week?  

**Geocoding functions must be used in HTTPS secure server.** 

* What excites or interests you about coding?
* What is a recent technical challenge you experienced and how did you solve it?
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
* Talk about your preferred development environment.
* Which version control systems are you familiar with? * 

**Github** 

* Can you describe your workflow when you create a web page?
* If you have 5 different stylesheets, how would you best integrate them into the site?
* Can you describe the difference between progressive enhancement and graceful degradation?
* How would you optimize a website's assets/resources?
* How many resources will a browser download from a given domain at a time?
  * What are the exceptions?
* Name 3 ways to decrease page load (perceived or actual load time).
* If you jumped on a project and they used tabs and you used spaces, what would you do?
* Describe how you would create a simple slideshow page.
* If you could master one technology this year, what would it be?
* Explain the importance of standards and standards bodies.
* What is Flash of Unstyled Content? How do you avoid FOUC?
* Explain what ARIA and screenreaders are, and how to make a website accessible.
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
* What does CORS stand for and what issue does it address?

#### HTML Questions:

* What does a `doctype` do?  

**The doctype declaration should be the very first thing in an HTML document, before the tag. The doctype declaration is not an HTML tag; it is an instruction to the web browser about what version of the markup language the page is written in. The doctype declaration refers to a Document Type Definition (DTD).** 

* What's the difference between full standards mode, almost standards mode and quirks mode?  

**Layout engines in browsers uses three modes:
Quirks mode: In quirks mode, layout emulates nonstandard behavior in Navigator 4 and IE 5. These were needed for websites written before introduction of web standards. 
Full standard mode: In this mode, the behavior described is same as described by HTML and CSS specifications. Most of the modern browsers uses full standard mode.  
Almost standard Mode: In almost standard mode there is very small number of quirks implementation.    
https://neal.codes/blog/front-end-interview-questions-html/** .

* What's the difference between HTML and XHTML?  

**Broadly, the XML rules require that all elements be closed, either by a separate closing tag or using self-closing syntax (e.g. `<br />`), while HTML syntax permits some elements to be unclosed because either they are always empty (e.g. `<input>`) or their end can be determined implicitly ("omissibility", e.g.`<p>`) 
XML is case-sensitive for element and attribute names, while HTML is not.  
https://neal.codes/blog/front-end-interview-questions-html/**   

* Are there any problems with serving pages as `application/xhtml+xml`?  

**It will more than likely mess up the page for anyone still using older versions of IE. When a browser reads XML it uses an XML parser, not an HTML parser .   
https://neal.codes/blog/front-end-interview-questions-html/** .  

* How do you serve a page with content in multiple languages?  

**Always use a language attribute on the html tag to declare the default language of the text in the page. When the page contains content in another language, add a language attribute to an element surrounding that content.  
Always use a language attribute on the html element. This is inherited by all other elements, and so will set a default language for the text in the document head element.  
If your document is HTML (ie. served as text/html), use the lang attribute to set the language of the document or a range of text. For example, the following sets the default language to French: `<html lang="fr">`** 

* What kind of things must you be wary of when design or developing for multilingual sites?  

**Properly localizing content for different audiences based on their location, as well as allowing for a user to easily change their country/language.**  

* What are `data-` attributes good for?  

**Storing data in HTML for DOM parsing, or other ways of keeping track of information.** . 

* Consider HTML5 as an open web platform. What are the building blocks of HTML5?  

`<article>`
`<aside>`
`<audio>`
`<canvas>`
`<figcaption>`
`<figure>`
`<footer>`
`<header>`
`<hgroup>`
`<output>`
`<section>`
`<video>`   
  **The numerous APIs and the more semantic tags, could also be said to be the building blocks** 

* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.  

**Cookie:
Max size of 4093 bytes
Can set expiration date
Sent on every request
sessionStorage:
Max size of 2.5MBs+ depending on browser
Stored in browser and not sent with every request
If you close a tab using sessionStorage, open a new tab, or exit the browser - you'll lose that specific sessionStorage data.
localStorage:
Max size of 2.5MBs+ depending on browser
Stored in browser and not sent with every request
Will persist if browser/tabs are closed.** 

* Describe the difference between `<script>`, `<script async>` and `<script defer>`.  

**A regular `<script>` tag will block rendering of the page, and the page will not continue to load until the script finishes.
`<script async>` will run the script asynchronously, meaning that it will not block rendering, but will run as soon as the script is available. This is usually intended for CDN files, or other such files, which do not change the page structure.
`<script defer>` will defer the script to run after the page is done parsing and before an onload event.**  
  
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?  

**You usually put the `<link>` tags in between the `<head>` to prevent Flash of Unstyled Content which gives the user something to look at while the rest of the page is being parsed.  
Since Javascript blocks rendering by default, and the DOM and CSSOM construction can be also be delayed, it is usually best to keep scripts at the bottom of the page.  
Exceptions are if you grab the scripts asynchronously, or at least defer them to the end of the page.**  

* What is progressive rendering?  

**Progressive rendering is the name given to techniques used to render content for display as quickly as possible. It used to be much more prevalent in the days before broadband internet but it's still useful in modern development as mobile data connections are becoming increasingly popular (and unreliable!)**  

* Have you used different HTML templating languages before?  

**A website template is a pre-built website composed of HTML pages that include integrated images, text content and support files for font styles and Javascripts.  
 Django (Python), ERB/Haml (Ruby), and Smarty (PHP)** 

#### CSS Questions:

* What is the difference between classes and IDs in CSS?  

**Unlike the id selector, the class selector is most often used on several elements. This allows you to set a particular style for many HTML elements with the same class. The class selector uses the HTML class attribute, and is defined with a "." id is used when we have to apply CSS property to one attribute only.** . 

* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?  

**Normalizing means to make a consistent look and feel of document styles for various browsers, while resetting is to clear the default CSS style of DOM elements.
https://yujianmin.wordpress.com/tag/css-interview-questions/**

* Describe Floats and how they work.  

**Float defines whether or not an element should float (left/right). In the simplest usage, the float can be used to wrap text around a image.  
Float affects not only  the target element, but also its children.**


* Describe z-index and how stacking context is formed.  

**The z-index property specifies the stack order of an element, an element with greater stack order is always in front of an element with a lower stack order. Say two DIVs with the same parent, higher z-index will be displayed. It will inherit the z-index property of the parent. Z-index only works on positioned elements (position:absolute, position:relative, or position:fixed). Value can be negative.** 

* Describe BFC(Block Formatting Context) and how it works.  

**A BFC is part of the visual CSS rendering of a web page in which block boxes are laid out. For effectively creating the block content, applying CSS like overflow: scroll/hidden, display: inline-block/flex/table, float:left/right to the container.
In a block formatting context, each box’s left outer edge touches the left edge of the containing block (for right-to-left formatting, right edges touch).** 

* What are the various clearing techniques and which is appropriate for what context?  

**a. Create an empty DIV:  
b. Set overflow: setting auto or hidden overflow property on parent will expand it to contain the floats.  
c. Use psuedo class: uses the parent’s :after to add the clear: both property 
.clearfix:after { 
content: “”;  
visibility: hidden;  
display: block;  
height: 0;  
clear: both;  
}** 

* Explain CSS sprites, and how you would implement them on a page or site.  

**CSS sprites is the technique to combine all individual images into one big image so that it can help reduce HTTP requests and data size.  
Usually, you don’t know how many images you need at the beginning, so it will be done at the stage of production launch. Locating of individual images is by using background image position index.** 

* What are your favourite image replacement techniques and which do you use when?  

**CSS image replacement is a technique of replacing a text element (usually a header tag) with an image. An example of this would be including a logo on a page. You may want to use a `<h1>` tag and text for this for the accessibility and SEO benefits, but ideally you’d like to show your logo, not text.** 

* How would you approach fixing browser-specific styling issues?

**a. Use normalized CSS library 
b. Implement vendor specific CSS fix 
c. Test in all targeted browsers** 

* How do you serve your pages for feature-constrained browsers? 
* What techniques/processes do you use?

**a. Reduce content and layout for feature-constrained browsers.  
b. Add vendor-specific CSS fixes to the pages 
c. Media query, browser detection (buggy)** 


  
* What are the different ways to visually hide content (and make it available only for screen readers)?
* Have you ever used a grid system, and if so, what do you prefer?
* Have you used or implemented media queries or mobile specific layouts/CSS?
* Are you familiar with styling SVG?
* How do you optimize your webpages for print?
* What are some of the "gotchas" for writing efficient CSS?
* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
* Explain how a browser determines what elements match a CSS selector.
* Describe pseudo-elements and discuss what they are used for.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
* List as many values for the display property that you can remember.
* What's the difference between inline and inline-block?
* What's the difference between a relative, fixed, absolute and statically positioned element?
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* Have you played around with the new CSS Flexbox or Grid specs?
* How is responsive design different from adaptive design?
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?

#### JS Questions:

* Explain event delegation
* Explain how `this` works in JavaScript
* Explain how prototypal inheritance works
* What do you think of AMD vs CommonJS?
* Explain why the following doesn't work as an IIFE: `function foo(){ }();`.
  * What needs to be changed to properly make it an IIFE?
* What's the difference between a variable that is: `null`, `undefined` or undeclared?
  * How would you go about checking for any of these states?
* What is a closure, and how/why would you use one?
* What's a typical use case for anonymous functions?
* How do you organize your code? (module pattern, classical inheritance?)
* What's the difference between host objects and native objects?
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
* What's the difference between `.call` and `.apply`?
* Explain `Function.prototype.bind`.
* When would you use `document.write()`?
* What's the difference between feature detection, feature inference, and using the UA string?
* Explain Ajax in as much detail as possible.
* What are the advantages and disadvantages of using Ajax?
* Explain how JSONP works (and how it's not really Ajax).
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
* Explain "hoisting".
* Describe event bubbling.
* What's the difference between an "attribute" and a "property"?
* Why is extending built-in JavaScript objects not a good idea?
* Difference between document load event and document DOMContentLoaded event?
* What is the difference between `==` and `===`?
* Explain the same-origin policy with regards to JavaScript.
* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
* What is `"use strict";`? what are the advantages and disadvantages to using it?
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
* Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
* Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
* Explain what a single page app is and how to make one SEO-friendly.
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* What tools and techniques do you use debugging JavaScript code?
* What language constructions do you use for iterating over object properties and array items?
* Explain the difference between mutable and immutable objects.
  * What is an example of an immutable object in JavaScript?
  * What are the pros and cons of immutability?
  * How can you achieve immutability in your own code?
* Explain the difference between synchronous and asynchronous functions.
* What is event loop?
  * What is the difference between call stack and task queue?
* Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`

#### Testing Questions:

* What are some advantages/disadvantages to testing your code?
* What tools would you use to test your code's functionality?
* What is the difference between a unit test and a functional/integration test?
* What is the purpose of a code style linting tool?

#### Performance Questions:

* What tools would you use to find a performance bug in your code?
* What are some ways you may improve your website's scrolling performance?
* Explain the difference between layout, painting and compositing.

#### Network Questions:

* Traditionally, why has it been better to serve site assets from multiple domains?
* Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.
* What are the differences between Long-Polling, Websockets and Server-Sent Events?
* Explain the following request and response headers:
  * Diff. between Expires, Date, Age and If-Modified-...
  * Do Not Track
  * Cache-Control
  * Transfer-Encoding
  * ETag
  * X-Frame-Options
* What are HTTP methods? List all HTTP methods that you know, and explain them.

#### Coding Questions:

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

*Question: What is the value of `window.foo`?*
```javascript
( window.foo || ( window.foo = "bar" ) );
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

#### Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Who inspires you in the front-end community?
* Do you have any pet projects? What kind?
* What's your favorite feature of Internet Explorer?
* How do you like your coffee?


#### Contributors:

This document started in 2009 as a collaboration of [@paul_irish](https://twitter.com/paul_irish) [@bentruyman](https://twitter.com/bentruyman) [@cowboy](https://twitter.com/cowboy) [@ajpiano](https://twitter.com/ajpiano)  [@SlexAxton](https://twitter.com/slexaxton) [@boazsender](https://twitter.com/boazsender) [@miketaylr](https://twitter.com/miketaylr) [@vladikoff](https://twitter.com/vladikoff) [@gf3](https://twitter.com/gf3) [@jon_neal](https://twitter.com/jon_neal) [@sambreed](https://twitter.com/sambreed) and [@iansym](https://twitter.com/iansym).

It has since received contributions from over [100 developers](https://github.com/h5bp/Front-end-Developer-Interview-Questions/graphs/contributors).
