# Add Todos to the Database from the Rails Console
The Rails console is a program we can run in our command line to talk to the database we just created. We can run the Rails console by typing in the following command:
```shell
$ rails console
```

The prompt is going to be slightly different, you should see a ruby version and an angle bracket at the end.

![Rails Console](/images/add_todos_to_the_database_from_the_rails_console/01.png "Rails Console")

The Rails console give us a test environment to try out Ruby code before we put it in our application.

## Adding Todo object to the database
You can add objects to your database from the Rails console. For example, if you wanted to add a new Todo object to the database you would use the following command:
```shell
> t = Todo.new
```

You're using an uppercase T for Todo because it’s a model. We’re assigning a new Todo object to a variable called t. Think of it as a new row being created in the database table.

![New Todo](/images/add_todos_to_the_database_from_the_rails_console/02.png "New Todo")

This tells you that a Todo object was created, but it hasn’t been saved to the database yet because the id is still nil.

You can assign this new Todo object a description. Use the following command to do so:
```shell
> t.description = "Make the curriculum"
```
You can also assign this Todo object a Pomodoro estimate. Use the following command:
```shell
> t.pomodoro_estimate = 4
```

Now that you've set the description and Pomodoro estimate of the new Todo object, you want to save it to the database. You can do that by using the following command;
```shell
> t.save
```

Now add your second Todo object to the database using the same method as demonstrated above.

>Give your students some time to complete this exercise.

Now let's see how many Todos we have saved in the database:
```shell
> Todo.all
```

If you want to find a Todo object with a particular id, let’s say an id of 1, use the following command:
```shell
> Todo.find_by_id(1)
```

## Move the process to the Todo controller show aciton
You can use the same process to find a specific List object in your database from your show action in the Todo controller. Navigate to the show action in your Todo controller. Enter the following code before your if statement:
```ruby
@todo = Todo.find_by_id(params[:id])
```

This will search the `todos` database table for a row with an id that matches the number the user entered at the end of the route in the URL.

Now that you have the `@todo` instance variable, open up the show.html.erb file and replace all of the places you have `@todo_description` and `@todo_pomodoro_estimate` with `@todo.description` and `@todo.pomodoro_estimate`. What’s happening here is we no longer need to store the instance variables with the Todo descriptions and Pomodoro estimates because we are pulling the info directly from the database.

Now it should look like so:
```ruby
<h2><%= @todo.description %></h2>
  <span class="pomodoro-estimate large-pomodoro-estimate"><%= @todo.pomodoro_estimate %> Pomodoros</span>
```
   
Now return to your live application and go to the URL ending in ***/todo/show/1***. Everything should work the same.

Now go ahead and get rid of all of your conditional statements in the show action and see what happens when you reload the page! Your code should now look something like the block below:
```ruby
def show
  @todo = Todo.find_by_id(params[:id])
end
```

Now try and go to the URL ***/todo/show/2***. Everything should work. Now try and visit ***/todo/show/3***. You will run into an error page that looks similar to the one below.

![No Method Error](/images/add_todos_to_the_database_from_the_rails_console/03.png "No Method Error")

Rails is showing us this error because we are asking it to display information on the page for a Todo with an ID of 3, when we only have two Todo objects store in our database. So we have to add more.

Returning to the command line is tedious though, and a slow way to add todos to our databases. In the next section, we're going to learn how to set up a form and create new todos straight from the browser.

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Remove conditional logic and pull data straight from the database"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
