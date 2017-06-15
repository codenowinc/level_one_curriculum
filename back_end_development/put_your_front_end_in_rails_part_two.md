# Put Your Front End In Rails - Part Two
Log in to your GitHub account and navigate to your todo_app_front_end repository. Once you are there, click the index.html file. You should be on a page that shows you the contents of your index.html file, like the one below.

![index.html](/images/put_your_front_end_in_rails_part_two/01.png "index.html")

In your index.html file on GitHub, copy all of of the HTML in between the `<body></body>` tags like in the image below.

![Copy the HTML](/images/put_your_front_end_in_rails_part_two/02.png "Copy the HTML")

Now paste that HTML into your index.html.erb file in your Rails Application, replacing the placeholder HTML you had in there from the previous section. Your index.html.erb file should look similar to the file below:

*index.html.erb*
```html.erb
<h1>
  <img class="company-logo" src="https://public.3.basecamp.com/p/iahgNshn1oKq98sWGf1q89Vo/uploads/511042491/download/CodeNow%20Logo.png"></img>
  Workshop Todo List
</h1>

<ul class="card">
  <li>
    <input type="checkbox" name=""/>
    <a href="show.html">Make the curriculum</a>
    <span class="pomodoro-estimate">4 Pomodoros</span>
  </li>
  <li>
    <input type="checkbox" name=""/>
    Buy workshop supplies
    <span class="pomodoro-estimate">3 Pomodoros</span>
  </li>
  <li>
    <input type="checkbox" name=""/>
    Meet with the volunteer trainers
    <span class="pomodoro-estimate">2 Pomodoros</span>
  </li>
  <li>
    <input type="checkbox" name=""/>
    Order food for Saturday and Sunday
    <span class="pomodoro-estimate">1 Pomodoro</span>
  </li>
  <li>
    <input type="checkbox" name=""/>
    Check pre-work assignments
    <span class="pomodoro-estimate">2 Pomodoros</span>
  </li>
  <li>
    <input type="checkbox" name=""/>
    Send workshop location to all the students
    <span class="pomodoro-estimate">1 Pomodoro</span>
  </li>
  <li>
    <input type="checkbox" name=""/>
    Have a great workshop
    <span class="pomodoro-estimate">0 Pomodoros</span>
  </li>
</ul>

<div id="new-todo-block">
  <input class="text-input" id="new-todo-description" type="text" placeholder="Add a new todo...">
  <input class="text-input" id="new-pomodoro-estimate" type="number" placeholder="Pomodoro estimate...">
  <input class="button" id="add-new-todo-button" type="submit" value="Add todo">
</div>
```
