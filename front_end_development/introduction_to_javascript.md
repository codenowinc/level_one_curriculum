# Introduction to JavaScript
Now that we've added our content, marked it up with tags (HTML), and styled it (CSS), we can learn how to make it a bit more interactive.

## Reivew
  * **HTML** is the markup language that we use to structure and give meaning to our web content, for example defining paragraphs, headings, and lists, or embedding images and videos on the page.

  * **CSS** is a language of style rules that we use to apply styling to our HTML content, for example setting background colors and fonts, and laying out our content on the page.

## What is JavaScript?
Simply put, JavaScript is a programming language that enables you to create dynamically updating content, control multimedia, animate images, and many other interactive features on your web page.

### The DOM API
What is even more exciting however is the functionality built on top of the core JavaScript language. So-called Application Programming Interfaces (APIs) provide you with extra superpowers to use in your JavaScript code.

APIs are ready-made sets of code building blocks that allow a developer to implement programs that would otherwise be hard or impossible to implement.

Today we'll be using the DOM (Document Object Model) API. It allows you to manipulate HTML and CSS, creating, removing and changing HTML, dynamically applying new styles to your page, etc. Everytime you see a popup window appear on a page, or some new content displayed (such as adding another todo to your list), that's the DOM in action.

### Back to JS
So what happens when you load a web page in a browser? When you load a web page in your browser, you are running your code (the HTML, CSS, and JavaScript) inside an execution environment (the browser tab). This is like a factory that takes in raw materials (the code) and outputs a product (the web page).

The JavaScript is executed by the browser's JavaScript engine, after the HTML and CSS have been assembled and put together into a web page. This ensures that the structure and style of the page are already in place by the time the JavaScript starts to run.

This is a good thing, as a very common use of JavaScript is to dynamically modify HTML and CSS to update a user interface, via the Document Object Model API (as mentioned above). If the JavaScript loaded and tried to run before the HTML and CSS was there to affect, then errors would occur.
