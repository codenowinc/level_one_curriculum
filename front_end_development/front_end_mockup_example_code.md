# Front End Mockup Example Code

>Here is the code up to this point for the Todo List App Front End Mockup. Have your students work towards this with their own mockups before moving on to other concepts and topics.

***index.html***
```HTML
<html>
  <head>
    <title>Todo List Application</title>
    <link rel="stylesheet" href="index.css" type="text/css"/>
  </head>

  <body>
    <h1>
      <img class="company-logo" src="https://public.3.basecamp.com/p/iahgNshn1oKq98sWGf1q89Vo/uploads/511042491/download/CodeNow%20Logo.png"></img>
      Workshop Todo List
    </h1>

    <ul>
      <li>
        <input type="checkbox">
        <a href="show.html">Make the curriculum</a>
        <span class="pomodoro-estimate">4 pomodoros</span>
      </li>
      <li>
        <input type="checkbox">
        Buy workshop supplies
        <span class="pomodoro-estimate">3 Pomodoros</span>
      </li>
      <li>
        <input type="checkbox">
        Meet with the volunteer trainers
        <span class="pomodoro-estimate">2 Pomodoros</span>
      </li>
      <li>
        <input type="checkbox">
        Order food for Saturday and Sunday
        <span class="pomodoro-estimate">1 Pomodoro</span>
      </li>
      <li>
        <input type="checkbox">
        Check pre-work assignments
        <span class="pomodoro-estimate">2 Pomodoros</span>
      </li>
      <li>
        <input type="checkbox">
        Send workshop location to all the students
        <span class="pomodoro-estimate">1 Pomodoro</span>
      </li>
      <li>
        <input type="checkbox">
        Have a great workshop
        <span class="pomodoro-estimate">0 Pomodoros</span>
      </li>
    </ul>

    <div>
      <input type="text" placeholder="Add a new todo...">
      <input type="number" placeholder="Pomodoro estimate...">
      <input id="add-new-todo-button" type="submit" value="Add todo">
    </div>
  </body>
</html>
```

***index.css***
```CSS
body{
 color: #424242;
 background-color: #ECEFF1;
 font-family: sans-serif;
}

h1{
  color: #03A9F4;
  text-align: center;
  margin-top: 20px;
}

img{
  width: 150px;
}

ul{
  list-style: none;
  font-size: 20px;
  background-color: #FFF;
  padding: 20px;
  width: 60%;
  margin: 0 auto;
  border-radius: 5px;
  box-shadow: 1px 1px 1px #90A4AE;
}

li{
  margin-bottom: 10px;
  padding: 5px;
}

li:hover{
  background-color: #E1F5FE;
  border-radius: 3px;
}

a{
  text-decoration: none;
  color: #424242;
  vertical-align: middle;
}

div{
  width: 60%;
  margin: 20px auto 0px auto;
}

input[type="text"], input[type="number"]{
  font-size: 20px;
  background-color: #FFF;
  outline: none;
  border-style: none;
  padding: 5px;
  border-radius: 3px;
  box-shadow: 1px 1px 1px #90A4AE;
}

.pomodoro-estimate{
  font-weight: bold;
  color: #F44336;
  background-color: #F5F5F5;
  border-radius: 50px;
  font-size: 14px;
  padding: 5px 10px 5px 10px;
}

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

#add-new-todo-button:active{
  box-shadow: 1px 1px 1px #90A4AE;
}
```
