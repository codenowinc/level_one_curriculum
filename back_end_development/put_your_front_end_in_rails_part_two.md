# Put Your Front End In Rails - Part Two

## Add the HTML
Log in to your GitHub account and navigate to your todo_app_front_end repository. Once you are there, click the index.html file. You should be on a page that shows you the contents of your index.html file, like the one below.

![index.html](/images/put_your_front_end_in_rails_part_two/01.png "index.html")

In your index.html file on GitHub, copy all of of the HTML in between the `<body></body>` tags like in the image below.

![Copy the HTML](/images/put_your_front_end_in_rails_part_two/02.png "Copy the HTML")

Now paste that HTML into your index.html.erb file in your Rails Application, replacing the placeholder HTML you had in there from the previous section. Your index.html.erb file should look similar to the file below:

***index.html.erb***
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

The reason we only add the HTML within the body tags is that Rails automatically adds the HTML document structure tags for us by loading the application.html.erb file located at ***app/layouts/application***. If you navigate to this html.erb file, you'll see all of the HTML document structure tags.

When Rails loads a web page, it always loads this file first, and then the view file you write. The HTML from your html.erb file is then inserted where it says `<%= yield %>`. We will learn more about this concept later.

Now return to your live app, and refresh the browser. You should see your todo list index page!

![Rendered HTML](/images/put_your_front_end_in_rails_part_two/03.png "Rendered HTML")



## Add the CSS
Now that we have our index page HTML in our Rails App, let's drop in our CSS. Rails makes adding CSS to our application easy on us by giving us one place to put all of our styles for the whole application. And better yet, everything is already linked.

In your file tree, navigate to the ***app/assets/stylesheets*** directory and open application.css. You'll see some commented out text in the file, do not get rid of it.

Return to your todo_app_front_end repository on GitHub, and navigate to your index.css file.

![index.css](/images/put_your_front_end_in_rails_part_two/04.png "index.css")

Copy the CSS code from index.css, and paste it into application.css in your Rails App, below the commented out text, on line 16. Your file should look similar to the one below:

***application.css***
```css
ul{
  list-style: none;
  font-size: 20px;
}

li{
  margin-bottom: 10px;
  padding: 5px;
}

li:hover{
  background-color: #E1F5FE;
  border-radius: 3px;
}

span{
  font-size: 14px;
  padding: 5px 10px 5px 10px;
}

.completed-todo{
  text-decoration: line-through;
}

#new-todo-block{
  width: 60%;
  margin: 20px auto 0px auto;
}

#add-new-todo-button{
  display: block;
  background-color: #03A9F4;
  margin-top: 10px;
}
```

Rails will use this one application.css file to hold all of the CSS for the entire application. Remember, CSS compiles from top to bottom. This means if you have the same element styled twice in your CSS, the style rules lower down in the file will be the ones that are applied.

Now return to your live app, and refresh the browser. You should see your todo list index page fully styled just like your front end mock up!

![Styled HTML](/images/put_your_front_end_in_rails_part_two/05.png "Styled HTML")

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add HTML and CSS from front end mockup to application"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
