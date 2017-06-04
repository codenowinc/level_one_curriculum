# Mark a Todo Complete

>Before starting this section, have your students create a new index.js file using the `touch` command.

*index.html*
```HTML
<html>
  <head>
    <title>Todo Index | Todo List Application</title>
    <link rel="stylesheet" href="style.css" type="text/css" />
    <link rel="stylesheet" href="index.css" type="text/css" />
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
    <script type="text/javascript" src="index.js"></script>
  </head>

  <body>
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
  </body>
</html>
```

*index.css*
```CSS
.completed-todo{
  text-decoration: line-through;
}
```

*index.js*
```JavaScript
$(document).ready(function() {
  // Strike through todo when its checkbox is clicked
  $("ul").on("click", "input[type=checkbox]", function(){
    $(this).closest("li").toggleClass("completed-todo")
  })
})
```
