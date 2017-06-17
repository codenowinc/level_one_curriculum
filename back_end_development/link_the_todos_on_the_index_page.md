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
