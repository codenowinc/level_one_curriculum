# Link the Todos on the Index Page
Now that we have individual routes dynamically generated for each of our todos, we can link the todos on our index page to their show pages!

Right now, only the first todo on our index page is linked.
```html.erb
<li>
  <input type="checkbox" name=""/>
  <a href="show/1">Make the curriculum</a>
  <span class="pomodoro-estimate small-pomodoro-estimate">4 Pomodoros</span>
</li>
```

We can see the `<a></a>` tag wrapping the todo information so when we click "Make the curriculum" on the index page it takes us to the show page for that todo.

Go ahead and link the rest of your todos to their show pages by using the appropriate HTML tag and routes.

>Give your students some time to complete this activity.

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add links to todos on the index page"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
