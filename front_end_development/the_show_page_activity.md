# The Show Page Activity
Now that we've added and tagged all of our content in our index.html files, it's time to create a show page for the first todo in our list. The purpose of the show page is to display the information of a single todo in detail, and allow the user to perform some additional functionality that they are not able to to perform directly from the todo list on our index page.

Open your show.html file in Cloud9, and add the HTML document structure tags and a title for your show page. Then, in the body section of your HTML document, add the content for the description of the todo, the pomodoro estimate, a link to edit the todo, a link to delete the todo, and a link to go back to the index page. Make sure to tag all of your content semantically.

>Give your students time to complete this portion of the activity. They are going to have many questions, and will need help. Tell them to reference their index.html file when they are stuck or not sure how to proceed. You can use the HTML code below as a guide for what their code should look like when they are done.

*show.html*
```HTML
<html>
  <head>
    <title>Todo List Application</title>
  </head>
  <body>
    <input type="checkbox">
    <h2>Make the curriculum 4 Pomodoros</h2>
    <a href="#">Edit</a>
    <a href="#">Delete</a>
    <a href="#">Go back...</a>
  </body>
</html>
```
After you've added your content and tags to your show.html file, run your server in Cloud9 and view your show page live.

## Link Back to the Index Page
Now it would be cool if we could click the "Go back..." link and it actually took us back to the Index page. All we have to do is enter a path instead of a "#" after the href attribute (href stand for hyperlink reference) for "Go back...". The page we want to go back to is index.html so our `<a href=""></a>` tag is going to look something like this:
```HTML
<a href="index.html">Go back...</a>
```

>Give your students a moment to updat their `<a></a>` tags in their show.html files. After they get that link working, have them link to the show page from the appropriate todo in the index.html file. For example, the first todo in our example Todo List Application's index.html file would now link to this new show page, and the code would look like the following block:

```HTML
<li>
  <a href="show.html">Make the curriculum</a> 4 pomodoros
</li>
```

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add and tag content for show page"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
