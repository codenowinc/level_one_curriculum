# Different Tags for Different Content
So far, we have one big block of content in our index.html file. In that block, we have the name of the page, we have our list of todos, and we have the "Add todo" content that's supposed to allow us to add a new todo to our list.

Using that description of the content and this [HTML tag reference resource on W3 schools](https://www.w3schools.com/TAgs/ "W3 HTML Element Reference"), see if you can properly tag all of the content inside of your body tags.

>Give your students time complete this exercise. Walk around your group and talk them through the logic of headers, lists, list items, inputs (type checkbox) and links. Explain how they should search for specific tags that are supposed to be used for specific content types. Remind them of the concept of semantic tagging. After this exercise, the code should look similar to the block below.

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
  </body>
</html>
```

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Tag all content"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.

