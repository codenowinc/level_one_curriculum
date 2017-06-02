# CSS Selectors
A CSS selector is the part of the CSS rule that selects the content you want to style. There are many CSS selectors, but for today, we are going to focus on the following:

## Selectors
  * Element Type Selector
  * Class Selector
  * ID Selector
  * Pseudo Class Selector

#### Element Type Selector
This selector can also be referred to simply as a “type selector." Type selectors must match an HTML element of the same name. For example, a selector of `ul` would match the HTML `<ul>` element. A `li` selector would match all the `<li>` elements in an HTML document.

We've already seen an example of applying a CSS style rule using a type selector:
```CSS
html{
  font-family: sans-serif;
}
```

#### Class Selector
The class selector is the selector you will probably use most when writing CSS. It’s declared with a dot or period preceding a string of one or more characters. The class selector also matches all HTML elements on the page that have their class attribute set to the same value as the class, minus the dot. Let's look at an example.

Let's say we want to highlight the Pomodoro estimates for each task, so they stand out from the rest of the information. We want every Pomodoro estimate to look the same as the next, but different from everything else on the page.

Right now, the HTML containing the content for the Pomodoro estimates looks like the code below:
```HTML
<li>
  <input type="checkbox">
  Buy workshop supplies 3 Pomodoros
</li>
```

The first step we'll need to take to apply some style the "3 Pomodoros" content is wrap it in HTML tags so we have a way to grab it. The tag we'll use in this case is the `<span>` tag. `<span>` tags are used for content that can't be defined traditionally. Our HTML will look as follows:
```HTML
<li>
  <input type="checkbox">
  Buy workshop supplies
  <span>3 Pomodoros</span>
</li>
```

Putting our `<span>` tag and the "3 Pomodoros" content on a seprate line will not change how it looks in the browser, it just makes our HTML easier to read. Go ahead and put span tags around all of your Pomodoros estimates in your index.html file.

>Give your students a few minutes to wrap all of their Pomodoro estimates in `<span>` tags. Their code should look like the block below when they are done.

*index.html*
```HTML
<html>
  <head>
    <title>Todo List Application</title>
    <link rel="stylesheet" href="index.css" type="text/css"/>
  </head>
  <body>
    <h1>Workshop Todo List</h1>
    <ul>
      <li>
        <input type="checkbox">
        <a href="show.html">Make the curriculum</a>
        <span>4 pomodoros</span>
      </li>
      <li>
        <input type="checkbox">
        Buy workshop supplies
        <span>3 Pomodoros</span>
      </li>
      <li>
        <input type="checkbox">
        Meet with the volunteer trainers
        <span>2 Pomodoros</span>
      </li>
      <li>
        <input type="checkbox">
        Order food for Saturday and Sunday
        <span>1 Pomodoro</span>
      </li>
      <li>
        <input type="checkbox">
        Check pre-work assignments
        <span>2 Pomodoros</span>
      </li>
      <li>
        <input type="checkbox">
        Send workshop location to all the students
        <span>1 Pomodoro</span>
      </li>
      <li>
        <input type="checkbox">
        Have a great workshop
        <span>0 Pomodoros</span>
      </li>
    </ul>

    <input type="text" placeholder="Add a new todo...">
    <input type="number" placeholder="Pomodoro estimate...">
    <input type="submit" value="Add todo">
  </body>
</html>
```
Now let's learn how to apply a class attribute to an HTML element. Class attributes are written in the same way as the placeholder and type attributes we learned about earlier. In the opening tag of your HTML `<span>` tag write `class=""`. What goes inside the quotes is a string describing the content. In this case, our class would look something like this:
```HTML
<li>
  <input type="checkbox">
  Buy workshop supplies
  <span class="pomodoro-estimate">3 Pomodoros</span>
</li>
```

>Give your students some time to apply the pomodoro-estimate class attribute to the first `<span>` tag in their index.html document.

We can now use this class selector in our index.css document to apply style rules to our Pomodoro estimate. Unlike element type selectors, class selectors must be called after a . when used to define a rule. For example, to define a rule using the pomodoro-estimate class we just defined, the code in your index.css file would look like the following:
```CSS
.pomodoro-estimate{

}
```

Now let's add some styles!
```CSS
.pomodoro-estimate{
  font-weight: bold;
  color: #F44336;
  background-color: #F5F5F5;
  border-radius: 50px;
  font-size: 14px;
  padding: 5px 10px 5px 10px;
}
```

Feel free to explore these style properties and play around with them.

>Give your students some time to play around with the CSS properties.

If we refresh our live web page, we see that the CSS style rules have only been applied to a single Pomodoro estimate. In order to apply the styles to all of our Pomodoro estimates, we need not write more CSS, but apply the same class attribute to all of the `<span>` elements wrapping our Pomodoro estimates in our index.html document.

>Give you students some time to apply the `pomodoro-estimate` class to all of the `<span>` tags.

A class can be applied to as many HTML tags as needed.

#### ID Selector
An ID selector is declared using a hash, or pound symbol (#) preceding a string of characters. This selector matches an HTML element that has an ID attribute with the same value as that of the selector.

Let's practice by adding the following id attribute to the `<<input type="submit"> HTML element in our index.html file.
```HTML
<input id="add-new-todo-button" type="submit" value="Add todo">
```

Like class attributes, the name of an id attribute should be descriptive of the content. Unlike a class though, an id should only be used on one single piece of content. This is what is known as best practice. In the above example, the id `add-new-todo-button` should not be used anywhere else in your HTML.

Now let's apply some CSS style rules to this `<input>` element using its id.
```CSS
#add-new-todo-button{
  font-size: 20px;
  text-align: center;
  color: #FFF;
  outline: none;
  border-style: none;
  padding: 10px;
  border-radius: 3px;
  box-shadow: 2px 2px 1px #90A4AE;
  display: block;
  background-color: #03A9F4;
  margin-top: 10px;
}
```

Once again, feel free to play around with the CSS properties. You only learn by trying whatever comes to mind!

>Give your students some time to play with the styles.

#### Pseudo-Class Selector
A pseudo-class uses a colon character to identify a pseudo-state that an element might be in—for example, the state of being hovered, or the state of being clicked or activated. Sometimes, we want a certain style rule applied to an element only when something specific has happened to that element. For example, wouldn't it be cool to make the button we just styled look like it was being pushed down when it was clicked? We can!

Use a psuedo-class selector by using the element type, class, or id (however you're referring to the HTML element) and a colon follwed by the action or state of the element during which you want the style applied.
```CSS
#add-new-todo-button:active{
  box-shadow: 1px 1px 1px #90A4AE;
}
```

Now refresh your web browser and see what happens when you click the "Add todo" button!

>Give your student to experiment with the pseudo-selector and test the button.

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add various CSS selectors"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.

