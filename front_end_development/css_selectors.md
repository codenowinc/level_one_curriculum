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
The class selector is the selector you will probably use most when writing CSS. It’s declared with a dot preceding a string of one or more characters. The class selector also matches all HTML elements on the page that have their class attribute set to the same value as the class, minus the dot. Let's look at an example.

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


#### ID Selector

#### Pseudo Class Selector

[CSS Selectors Resource](https://www.sitepoint.com/web-foundations/css-selectors/ "CSS Selectors Resource")
