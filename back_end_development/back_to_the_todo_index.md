# Back to the Todo Index
Phew! It's been a long day! We've made it through a lot. We've just completed six out of the seven golden actions. All we have todo is get the todos in our Database to show up on our Index page. right now, we still have our hard coded todos. We're going to make things really simple.

This is what our current index.html.erb file looks like:

***index.html.erb***
```html.erb
<ul class="card">
<li>
  <input type="checkbox" name=""/>
  <a href="show/1">Make the curriculum</a>
  <span class="pomodoro-estimate small-pomodoro-estimate">4 Pomodoros</span>
</li>
<li>
  <input type="checkbox" name=""/>
  <a href="show/2">Buy workshop supplies</a>
  <span class="pomodoro-estimate small-pomodoro-estimate">3 Pomodoros</span>
</li>
<li>
  <input type="checkbox" name=""/>
  <a href="show/3">Meet with the volunteer trainers</a>
  <span class="pomodoro-estimate small-pomodoro-estimate">2 Pomodoros</span>
</li>
<li>
  <input type="checkbox" name=""/>
  <a href="show/4">Order food for Saturday and Sunday</a>
  <span class="pomodoro-estimate small-pomodoro-estimate">1 Pomodoro</span>
</li>
<li>
  <input type="checkbox" name=""/>
  <a href="show/5">Check pre-work assignments</a>
  <span class="pomodoro-estimate small-pomodoro-estimate">2 Pomodoros</span>
</li>
<li>
  <input type="checkbox" name=""/>
  <a href="show/6">Send workshop location to all the students</a>
  <span class="pomodoro-estimate small-pomodoro-estimate">1 Pomodoro</span>
</li>
<li>
  <input type="checkbox" name=""/>
  <a href="show/7">Have a great workshop</a>
  <span class="pomodoro-estimate small-pomodoro-estimate">0 Pomodoros</span>
</li>
</ul>

<div id="new-todo-block">
<a href="/todo/new" class="button add-new-todo-button" id="add-new-todo-button">Add a todo</a>
</div>
```

As we can see, we have a seven todos hardcoded. I want to be able to display as many todos as I have in my database, without having to write any additional HTML. In fact, I want to remove a majority of this HTML. What if we could use conditional statements, instance variables, and embedded ruby to display all of my todos in a list? We can!

## Simplifying your HTML
Lets start by paring down our HTML to just one todo.

***index.html.erb***
```html.erb
<ul class="card">
<li>
  <input type="checkbox" name=""/>
  <a href="show/1">todo.description</a>
  <span class="pomodoro-estimate small-pomodoro-estimate">4 Pomodoros</span>
</li>
</ul>

<div id="new-todo-block">
<a href="/todo/new" class="button add-new-todo-button" id="add-new-todo-button">Add a todo</a>
</div>
```

Now that we have simplified our HTML, let's replace our content with variables.
