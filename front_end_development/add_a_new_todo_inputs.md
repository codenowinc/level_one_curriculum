# Add a New Todo Inputs
The index page currently lists all of the todos we have written in our index.html files, but what if we want to add a new todo?

HTML isn't just for tagging content that is displayed to the user through the webpage, but can be used to accept content from the user as well.

To add a new todo to our list, there are two pieces of information the user needs to provide: a description of the todo, and the number of Pomodoros they think it will take to complete the task.

## The HTML Input Tag
To accept input from the user, we can use the `<input>` HTML tag. The `<input>` tag is one of the few self closing tags in HTML, meaning that it does not have an opening and closing tag like all of the other tags we've seen so far.

All HTML tag elements can be given what are known as attributes. An attribute either modifies the default functionality of an HTML tag, or provides functionality to the tag without which it would be unable to function correctly. In HTML syntax, an attribute is added to an HTML start tag.

The `<input>` tag has a few attributes that we need to know about.

#### `type=""`
The type attribute allows us to tell HTML what kind of information we are trying to gather from the user. To add a new todo, we need the user to enter some text describing the todo, and we need them to enter a number estimating how many Pomodoros it will take to complete the task. So in this case, we are going to create two `<input>` tags and each one is going to have a type attribure with a different value. The HTML will look like the following code:
```HTML
<input type="text">
<input type="number">
```

In the code example, we can see the basic syntax for adding an attribute to an HTML tag.

Go ahead and add these two input HTML elements to the end of your index.html file.

>Give your student time to add their `<input>` tags to the end of their index.html files. Their code should look like the following block:

*index.html*
```HTML
<html>
  <head>
    <title>Todo List Application</title>
  </head>
  <body>
    <h1>Workshop Todo List</h1>
    <ul>
      <li>
        <input type="checkbox">
        Make the curriculum 4 pomodoros
      </li>
      <li>
        <input type="checkbox">
        Buy workshop supplies 3 pomodoros
      </li>
      <li>
        <input type="checkbox">
        Meet with the volunteer trainers 2 pomodoros
      </li>
      <li>
        <input type="checkbox">
        Order food for Saturday and Sunday 1 pomodoro
      </li>
      <li>
        <input type="checkbox">
        Check pre-work assignments 2 pomodoros
      </li>
      <li>
        <input type="checkbox">
        Send workshop location to all the students 1 pomodoro
      </li>
      <li>
        <input type="checkbox">
        Have a great workshop 0 pomodoros
      </li>
    </ul>

    <input type="text">
    <input type="number">
  </body>
</html>
```

If you run your server and look at your index.html file live, you'll notice two text boxes at the bottom of your page into which you can type information into. In fact, the second box also has an up and down arrow on the right side to toggle numbers, and you can't type any characters into this box. HTML knows only numbers are supposed to be entered into this input field!

But, if a user saw these two input boxes, they may have trouble figuring out what they are supposed to enter, so let's make it easier on them by giving them some context.

#### `placeholder=`
We want them to know what information they are supposed to enter into each input field. We can do this by adding another attribute to each input tag. This time the attribute we want to use is called placeholder. Let's see how it works.

Edit your `<input>` tags so they look like the following code:
```HTML
<input type="text" placeholder="Add a new todo...">
<input type="number" placeholder="Pomodoro estimate...">
```

> Give your students a moment to update their `<input>` tags.

Run your server and look at your input fields. Try entering information into the fields, what happens to the placeholders?

#### `<input type="submit">`
Finally, we need to give our users a way to submit the information after they've entered it into the input fields. There is a third type of input we can use for this, it is called `<input type="submit">`.

Add the following code right after your other two `<input>` tags. the `value=` attribute is the text that will go on the submit button.
```HTML
<input type="submit" value="Add todo">
```

>Give your students time to add the final `<input>` tag to their index.html files and test out the functionality. This steps final version of the index.html can be found below.

*index.html*
```HTML
<html>
  <head>
    <title>Todo List Application</title>
  </head>
  <body>
    <h1>Workshop Todo List</h1>
    <ul>
      <li>
        <input type="checkbox">
        Make the curriculum 4 pomodoros
      </li>
      <li>
        <input type="checkbox">
        Buy workshop supplies 3 pomodoros
      </li>
      <li>
        <input type="checkbox">
        Meet with the volunteer trainers 2 pomodoros
      </li>
      <li>
        <input type="checkbox">
        Order food for Saturday and Sunday 1 pomodoro
      </li>
      <li>
        <input type="checkbox">
        Check pre-work assignments 2 pomodoros
      </li>
      <li>
        <input type="checkbox">
        Send workshop location to all the students 1 pomodoro
      </li>
      <li>
        <input type="checkbox">
        Have a great workshop 0 pomodoros
      </li>
    </ul>

    <input type="text" placeholder="Add a new todo...">
    <input type="number" placeholder="Pomodoro estimate...">
    <input type="submit" value="Add todo">
  </body>
</html>
```
And that's the first step adding a new todo to our lists!

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add inputs to prepare for adding additional todos to todo list"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.

