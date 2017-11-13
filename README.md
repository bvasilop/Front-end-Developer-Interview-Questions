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
c. Use psuedo class: uses the parent’s :after to add the clear: both property**    

.clearfix:after { 
content: “”;  
visibility: hidden;  
display: block;  
height: 0;  
clear: both;  
}

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

**CSS display:none and/or visibility:hidden**
**Classic Method:** 
  `.hidden {  
    position: absolute;   
    left:-10000px;    
    top: auto;    
    width: 1px;    
    height: 1px;    
    overflow: hidden;    
    }` 
`<div class="hidden">Hidden content here.</div>`

**New Method:** 
  `hidden {  
  position: absolute;    
  clip: rect(0px 0px 0px 0px);    
}` 

`hidden {   
  position: absolute;     
  clip: rect(0px 0px 0px 0px);    
}`  
**Invisible Content**
`visibility: hidden; and/or display:none;`

* Have you ever used a grid system, and if so, what do you prefer?  

**Yes. Bootstrap, MUI CSS**

* Have you used or implemented media queries or mobile specific layouts/CSS?  

**Yes. Using Media Queries**

* Are you familiar with styling SVG?

**Not much experience in SVG except generating SVG images from JPG/PNG**

* How do you optimize your webpages for print?

**The simplest method is to create a style sheet for print only and test it well.

**e.g `<link rel=”stylesheet” type=”text/css” href=”/print.css” href=”/print.css” media=”print” />` 
Some steps:  
Format heading and paragraph tags, links and tables, clear unnecessary contents and images.** 

* What are some of the "gotchas" for writing efficient CSS?

**a. Know different browsers have different CSS hacks 
b. Cater for mobile devices or small screen size 
c. Good HTML structure and CSS OOP rules with good naming  
d. Avoid key selectors that match large numbers of elements (tag and universal selectors) 
e. Prefer class and ID selectors over tag selectors 
f. Avoid redundant selectors 
g. Preferably don’t use * (universal selector) 
h. Use framework (Bootstrap etc.)** 

* What are the advantages/disadvantages of using CSS preprocessors?
* Describe what you like and dislike about the CSS preprocessors you have used.  

**1. Debugging is harder 
2. Compilation slows down development 
3. Performance is compromised 
4. Maintainence and overengineering  
5. Tooling and developer convenience 
6. Saving generated files (or not) 
7. Capability and understanding 
Summary
It’s easy to add a CSS preprocessor to the tech stack. But, it’s not easy to remove it down the line, should we so choose.  
It’s our responsibility to consider the impact they have on our work flow before making the easy decision to install one.**
https://yujianmin.wordpress.com/tag/css-interview-questions/
http://blog.millermedeiros.com/the-problem-with-css-pre-processors/

* How would you implement a web design comp that uses non-standard fonts?

**Use @font-face or link the webfont url as CSS.** 
https://www.quora.com/What-is-the-best-way-to-use-non-standard-fonts-online 

* Explain how a browser determines what elements match a CSS selector.

**Browsers read selectors from right-to-left. First looks for all elements matching the key selector (the right-most). Then checks if it matches or is under the next (left-most) element.**

* Describe pseudo-elements and discuss what they are used for.

**Just like pseudo-classes, pseudo-elements are added to selectors but instead of describing a special state, they allow you to style certain parts of a document. For example, the ::first-linepseudo-element targets only  the first line of an element specified by the selector.** 

* Describe pseudo-elements and discuss what they are used for.  

**A CSS pseudo-class is a keyword added to selectors that specifies a special state of the element to be selected. For example :hover will apply a style when the user hovers over the element specified by the selector.  
Pseudo-classes, together with pseudo-elements, let you apply a style to an element not only in relation to the content of the document tree, but also in relation to external factors like the history of the navigator (:visited, for example), the status of its content (like :checked on some form elements), or the position of the mouse (like :hover which lets you know if the mouse is over an element or not).**

* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.

**For display purpose, every element in the page is considered a box. The box model refers to the specification of the box attributes such as the width, padding, border and margin. Some browsers (such as Firefox) think the width should only include the the content itself, not the padding, boarder, nor margin. Other browsers (such as IE) think the width should include the content, padding, and boarder, but not the margin.** 

**Content-box: width & height includes content but not padding/border/margin** 

**Padding-box: include up to padding** 

**Border-box: include up to border, but not margin** 

https://css-tricks.com/the-css-box-model/

* What does ```* { box-sizing: border-box; }``` do? What are its advantages?

**content-box:This is the initial and default value as specified by the CSS standard. The width and heightproperties are measured including only the content, but not the padding, border or margin. Note: Padding, border & margin will be outside of the box e.g. IF .box {width: 350px}; THEN you apply {border: 10px solid black;} RESULT {rendered in the browser} .box {width: 370px;}So simply the dimension of element is calculated as, width = width of the content, and height = height of the content (excluding the values of border and padding).      
border-box:The width and height properties include the padding and border, but not the margin. This is the box model used by Internet Explorer when the document is in Quirks mode. Note that padding and border will be inside of the box e.g.  .box {width: 350px; border: 10px solid black;} leads to a box rendered in the browser of width: 350px. The content box can’t be negative and is floored to 0, making it impossible to use border-box to make the element disappear.Here the dimension is calculated as, width = border + padding + width of the content, and height = border + padding + height of the content. The advantage of forcing all elements to adopt the border-box model is to unify the element width calculation regardless to browsers.**  

https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing

* List as many values for the display property that you can remember.

**block, inline, inline-block, none, inherit, table, table-cell, flex.**  

* What's the difference between inline and inline-block?

**inline-block: Displays an element as an inline-level block container. The inside of this block is formatted as block-level box, and the element itself is formatted as an inline-level box 
block:Displays an element as a block element**

* What's the difference between a relative, fixed, absolute and statically positioned element?

**relative: relative to itself, combine to use top/left.** 

**fixed: fixed at the position to the viewport, like top nav, no change when window scrolls.** 

**absolute: An element with this type of positioning is not affected by other elements and it doesn’t affect other elements.**  **You use it to position element to the exact location. It’s relative to the parent.** 
**static: default position** 
https://css-tricks.com/absolute-relative-fixed-positioining-how-do-they-differ/ 

*The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?


**Order in ascending order of importance:** 

**User agent declarations,  
User declarations,  
Author declarations,  
Author !important declarations,  
User !important declarations.** 
https://www.smashingmagazine.com/2010/04/css-specificity-and-inheritance/

* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?  

**Bootstrap. MUI. Can split out component by component by a tiny piece of CSS ?** 

* Have you played around with the new CSS Flexbox or Grid specs?

**The defining aspect of the flex layout is the ability to alter its items’ width and/or height to best fill the available space on any display device. A flex container expands items to fill available free space, or shrinks them to prevent overflow. For small-scale layout. A guide to flexbox.**

**Grid specs**
https://drafts.csswg.org/css-grid-1/

**For large-scale responsible layout. A guide to Grid CSS.** 
https://css-tricks.com/snippets/css/complete-guide-grid/


**CSS Flexbox** 
https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes

* How is responsive design different from adaptive design?

https://css-tricks.com/the-difference-between-responsive-and-adaptive-design/

https://www.uxpin.com/studio/blog/responsive-vs-adaptive-design-whats-best-choice-designers/

**Responsive is fluid and adapts to the size of the screen no matter what the target device. Responsive uses CSS media queries to change styles based on the target device such as display type, width, height etc., and only one of these is necessary for the site to adapt to different screens.**

**CSS Media queries**
https://developers.google.com/web/fundamentals/design-and-ux/responsive/?hl=en

**Adaptive design, on the other hand, uses static layouts based on breakpoints which don’t respond once they’re initially loaded. Adaptive works to detect the screen size and load the appropriate layout for it – generally you would design an adaptive site for six common screen widths (320,480,760,960,1200,1600)**

* Have you ever worked with retina graphics? If so, when and what techniques did you use?

**NO.  
Retina graphics.**

https://ivomynttinen.com/blog/a-guide-for-creating-a-better-retina-web

* Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?  
**No experience** 
https://www.paulirish.com/2012/why-moving-elements-with-translate-is-better-than-posabs-topleft/

*References
https://yujianmin.wordpress.com/tag/css-interview-questions/

#### JS Questions:

* Explain event delegation

**One of the hot methodologies in the JavaScript world is event delegation, and for good reason.  Event delegation allows you to avoid adding event listeners to specific nodes;  instead, the event listener is added to one parent.  That event listener analyzes bubbled events to find a match on child elements.**
https://davidwalsh.name/event-delegate
https://javascript.info/event-delegation

* Explain how `this` works in JavaScript
**The this keyword behaves differently in JavaScript compared to other language. In Object Oriented languages, the this keyword refers to the current instance of the class. In JavaScript the value of this is determined mostly by the invocation context of function (context.function()) and where it is called.**
**From what I understand, ‘this’ refers to itself, to its own object or global object.
Using ‘this’ are partitioned in 3 locations of code. These are in functions, outside of functions (global scope, ex: window object), and in Javascript’s eval() function.
Common pitfalls when using ‘this’ are usually relevant to scope issues in real functions, methods, and constructors. Though there are ways to fix these common issues by using ES5, bind() or ES6 arrow functions, =>**

http://2ality.com/2014/05/this.html
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this

* Explain how prototypal inheritance works

**A prototype is an internal object from which other objects inherit properties. Its main purpose is to allow multiple instances of an object to share a common property. Thus, object properties which are defined using the prototype object are inherited by all instances which reference it.**
https://www.htmlgoodies.com/html5/tutorials/javascript-prototypical-inheritance-explained.html
https://medium.com/@rlynjb/js-interview-question-explain-how-prototypal-inheritance-works-7537f98b8cd2

* What do you think of AMD vs CommonJS?  

**AMD and CommonJS are both Javascript module loader. They accomplish the same task but works different.
AMD is better for browser, hence, the name ‘Asynchronous’, as it loads each distinct module in async manner instead of loading in one large file. No extra steps are required to use AMD, it works out-of-the-box. In my opinion, as it is its in Asynchronous nature, it makes alot of async http requests and may not be as performant as described by other devs.
While, CommonJS, is a standard, mostly used in servers and it loads modules synchronously, though extra step is required if you want your JS file size to be minified and compressed.**
https://medium.com/@rlynjb/js-interview-question-what-do-you-think-of-amd-vs-commonjs-71defa831c50

* Explain why the following doesn't work as an IIFE: `function foo(){ }();` 

**What is IIFE?
An IIFE (pronouced as ‘iffy’) is an abbreviation for Immediately Invoked Function Expression. It is a common Javascript design pattern used by popular JS libraries such as jQuery, Backbone.js. Purpose of using an IIFE is to maintain code inside of a local scope. This means, to be able to use global object inside of IIFE, you will need to pass it as arguments.
As for an explanation, the following code doesn’t work as an IIFE because it is a function declaration, it does invoked immediately due to its parenthesis at the end, but there are downsides to using this approach.**
https://medium.com/@rlynjb/js-interview-question-explain-why-the-following-doesn-t-work-as-an-iife-1faaf74a7d7d


  * What needs to be changed to properly make it an IIFE?
  
  **For the above code to be considered an IIFE, it needs to be an anonymous function, a function without a name, this is because IIFE needs to be Invoked Immediately without invoking it a function name. We also need to wrap the anonymous function with parenthesis, so the Javascript parser treats our anonymous function as a function expression.
(function() {}());
A function expression is when you assign a function to a variable or property of an object. Anything that is a Javascript expression, including function expression, returns a value.**
https://medium.com/@rlynjb/js-interview-question-explain-why-the-following-doesn-t-work-as-an-iife-1faaf74a7d7d

* What's the difference between a variable that is: `null`, `undefined` or undeclared?  

**undefined is a variable that has been declared but no value exists and is a type of itself ‘undefined’.
null is a value of a variable and is a type of object.
We use ‘console.log();’ and ‘type of’ to check if a variable is undefined or null.
ref: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures
undeclared variables is a variable that has been declared without ‘var’ keyword.
testVar = ‘hello world’;
as opposed to
var testVar = ‘hello world’;
When former code is executed, undeclared variables are created as global variable and they are configurable (ex. can be deleted).**
https://medium.com/@rlynjb/js-interview-question-what-s-the-difference-between-a-variable-that-is-null-undefined-or-bf7233cef1c2


* How would you go about checking for any of these states?

**undefined is a variable that has been declared but no value exists and is a type of itself ‘undefined’.
null is a value of a variable and is a type of object.
We use ‘console.log();’ and ‘type of’ to check if a variable is undefined or null.
ref: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures
undeclared variables is a variable that has been declared without ‘var’ keyword.
testVar = ‘hello world’;
as opposed to
var testVar = ‘hello world’;
When former code is executed, undeclared variables are created as global variable and they are configurable (ex. can be deleted).**
https://medium.com/@rlynjb/js-interview-question-what-s-the-difference-between-a-variable-that-is-null-undefined-or-bf7233cef1c2
https://yehiaabed.com/blog/javascript-questions-answers/

* What is a closure, and how/why would you use one?  
**Closures are inner functions inside of an outer function. They have their own local scope and has access to outer function's scope, parameters (but NOT arguments object), and they also have access to global variables.** 
https://medium.com/@rlynjb/js-interview-question-what-is-a-closure-and-how-why-would-you-use-one-b6fd45ea95f6 

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

      // First declare for to describe loop  
      // Secondly declare a variable for i   
      // Then count through numbers one through 20 
      
    `for (var i = 1; i <= 20; i++) {`
    
      // Use if conditional to figure out if the numbers are divisible by 3, 5, or both.  
      // To simplify and condense code see if it is divisible by 15 --any number divisible by 3 and 5 is also divisible by 15--  
    `if(i % 15 === 0) {`   
      // If divisible by 15: Print FizzBuzz   
      `console.log('FizzBuzz');`   
      // Use else if conditional to determine if divisible by 3   
  `} else if (i % 3 ===0){`    
      // If only divisible by 3: Print Fizz    
      `console.log('Fizz');`  
      // Use else if conditional to determine if divisible by 5    
  `} else if (i % 5 === 0) {`   
      // If divisible by 5, Print Buzz    
      `console.log('Buzz');`  
      // Use else conditional to see if the number is not divisible by 3 or 5          
  `} else {`  
      // If it is not, then Print number    
      `console.log(i);`  
  `}   
}`

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
