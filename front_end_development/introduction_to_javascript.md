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

## Example
Let's try to write some JavaScript together! Open up [JSBin](http://jsbin.com/ "JSBin") and open the HTML, CSS, JavaScript, and Output tabs.

>Give your students a moment to navigate back to JSBin and open the appropriate tabs.

Cut and paste the following code into your HTML and CSS tabs respectively:

*JSBin HTML*
```HTML
<div>Player 1: NAME</div>
```

*JSBin CSS*
```CSS
div{
  font-family: 'helvetica neue', helvetica, sans-serif;
  letter-spacing: 1px;
  text-transform: uppercase;
  text-align: center;
  border: 2px solid rgba(0,0,200,0.6);
  background: rgba(0,0,200,0.3);
  color: rgba(0,0,200,0.6);
  box-shadow: 1px 1px 2px rgba(0,0,200,0.4);
  border-radius: 10px;
  padding: 3px 10px;
  display: inline-block;
  cursor:pointer;
}
```

>Give your students a moment to copy the code over to the appropriate tabs.

You should have a purple button with the text "Player 1: NAME" in your output tab.

Now let's write some JavaScript in our JavaScript tab in JSBin to change "NAME" to whatever name you actually want the button to display.

### Step One
In order to change the default "NAME" text to a name we actually want displayed, we need a way of asking the user to enter that information and we need a way of storing it. The first line of JavaScript we're going to right is going to define a variable that stores the `<div>` tag in which we want to change "NAME" to an actual name.

```JavaScript
var button_content = document.querySelector('div');
```

>Take this time to explain the concept of variables, scope, and storing various kinds of information.

### Step Two
Next, we need the User to be able to interact with the button and for the page to listen for the interaction. We want the user to be able to click the button, and get a prompt to enter in the actual name they want to replace "NAME" with. The first step in implementing this functionality is writing some code that tells the page to listen for the user's click of the button.

```JavaScript
button_content.addEventListener('click', updateName);
```

Here, we are telling JavaScript to register if the `<div>` is clicked. If it is clicked, JavaScript should execute a function called updateName. But what is updateName?

### Step Three
updateName is a function that we write. It is where we define what should happen when the user clicks the `<div>`. In this case, we want a prompt to show up for the user to enter in the actual name. We then want to save what they enter, and insert that name where it currently says "NAME" in the HTML.

```JavaScript
function updateName() {
  var name = prompt('Enter a new name');
  button_content.textContent = 'Player 1: ' + name;
}
```

Try it out!

>View the final JSBin snapshot [here](http://jsbin.com/pacatop/6/edit?html,css,js,output "Final JSBin Snapshot").
