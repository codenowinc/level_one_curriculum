# Many Show Pages, One View File

Let's take a look at our show.html.erb file again. It should something like this:
```html.erb
<h1>
  <img class="company-logo" src="https://public.3.basecamp.com/p/iahgNshn1oKq98sWGf1q89Vo/uploads/511042491/download/CodeNow%20Logo.png"></img>
  Workshop Todo List
</h1>

<div class="card">
  <input type="checkbox" name=""/>
  <h2><%= @todo_description %></h2>
  <span class="pomodoro-estimate large-pomodoro-estimate"><%= @todo_pomodoro_estimate %> Pomodoros</span>
  <a href="#" class="button" id="edit-todo-button">Edit</a>
  <a href="#" class="button" id="delete-todo-button">Delete</a>
  <a href="index" class="simple-link">Go back...</a>
</div>
```

We can see that there is no actual information about a specific todo in the HTML anymore. Our instance variables replaced the todo specific information. Now if there was a way to replace what was stored in our instance variables, so that we could see the show page for each todo in our list that would be great. And there is a way!

Right now, to access our show page in the browser, the user has to add **/todo/show** to the end of the URL. Their URL looks something like this:

![/todo/show](/images/many_show_pages_one_view_file/01.png "/todo/show")

This URL connects to the `get 'todo/show', to: 'todo#show'` in our routes.rb file. If we want a show page for every todo we add to our list, we're going to need a different route to take us to each specific page.

But the whole point of making things dynamic is to not have to write more code every time a new todo is added to the list. So what if there was a tool to automatically generate a new route for each todo?

## Dynamic Route Segments
Well, there is! And it's called a dynamic route segment. Starting to see a pattern here?

In our sample todo list application, we currently have seven todos. So to display a show page for each of these todos we need seven different routes - all related to show.

Let's say we number each todo 1-7. When we type **todo/show/1** into the URL, we want the show page for our first to show up, when we type **todo/show/2** into the URL, we want the show page for our second todo to show up, etc.

Right now, when we type **todo/show/1** into the URL all we get is an error:

![Routing error](/images/many_show_pages_one_view_file/02.png "Routing error")

If we go to our routes file and update our show page route from:
```ruby
get 'todo/show', to: 'todo#show'
```

to this:
```ruby
get 'todo/show', to: 'todo#show/1'
```

We see that going to **/todo/show/1** works!

![/todo/show/1](/images/many_show_pages_one_view_file/03.png "/todo/show/1")

But we're back in the same boat when we try to use **/todo/show/2**.

![Another routing error](/images/many_show_pages_one_view_file/04.png "Another routing error")

So instead of creating a separate route for each show page, we can add a variable to the end of our `get 'todo/show', to: 'todo#show'` route in our routes.rb file that accepts any number we type in to the URL bar. This variable is called a dynamic route segment.

We do this by coming up with a descriptive name for the variable. In this case, each todo is numbered 1-7 and so on. We can call these numbers ids. Each todo has an id which we can use to identify it. So if we enter **/todos/show/1** in the URL, we want to see the show page for the todo with an id of 1. If we enter **/todo/show/2** in the URL, we want to see the show page for the todo with an id of 2.

Adding the dynmaic route segment to our show page route in our routes.rb file looks like this:
```ruby
get 'todo/show/:id', to: 'todo#show'
```

If you did the Ruby tutorial homework, you'll remember that the colon `:` is used to define what are called symbols. Update your show page route.

>Give your students a moment to update their route to make it dynamic.

Now go to your live Rails application and add **/todo/show/1** to the end of your URL. Then try changing it to **/todo/show/1000**. Both of those work, even though you didn't create those routes explicitly. But they still render the same page. let's add some HTML and Ruby to our show.html.erb file to make what's happening more obvious.

Add the following code to the top of your show.html.erb file:
```html.erb
<h3>Todo #<%= params[:id] %></h3>
```

Now go to your live Rails application and add **/todo/show/1** to the end of your URL. Then try changing it to **/todo/show/1000**. You should see the number change! That is because, even though they look the same, they are actually two different pages. Now, how do we actually get todo number 2 to show up on the show page with the route **/todo/show/2**?

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add dynamic route segments"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
