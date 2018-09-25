# Edit, Update, and Delete
So you can add new items with a form but what if you need to update an existing list item in your database? It would be great if you could do that with a form as well. And you absolutely can!

We are now very familiar with the **RCAV** flow. So go ahead and complete the **RCAV** flow for the edit action, and the **RCA** flow for the update action. Just like the create action, we want the update action to direct the user to the show page of the todo that was just updated. So we don't need a view for the update action.

>Give your students some time to create the RCAV flow for edit and update. If you need to see an example of the code, you can visit [this commit](https://github.com/CodeNowOrg/todo_app_back_end/tree/734df28ccd0649e4d98815a8b5e7c5d895b89e96 "Edit and Update RCAV Flow") of the todo example app.

## Edit
The edit and update actions need a few extra pieces to make them work properly though. Rails needs to know which todo it's updating, find that todo in the database, and then populate the edit form with that information so the user knows what they are changing. Let's see how it works.

### Route
Just like the show action, we need to use a dynamic route segment in our edit and update routes so Rails knows which todo to edit and update. Your edit and update routes should look like the routes below:
```ruby
get 'todo/edit/:id', to: 'todo#edit'
```

### Controller & Action
Next, in the edit action, we have to create an instance variable called `@todo`. In `@todo` we'll store the todo we want to update. We'll be able to pass this specific todo through to the edit view so we can fill the edit form with the todo's existing information.
```ruby
def edit
  @todo = Todo.find_by_id(params[:id])
end
```

### View
Now we want to display a form that allows the user to edit the todo in the database. The form is going to look very similar to the form on the new page. With a few key differences.

***edit.html.erb***
```html.erb
<div class="card">
  <h2>Edit this todo...</h2>

  <form action="#">
    <input class="text-input" name="description" type="text" value="<%= @todo.description %>">
    <input class="text-input" name="pomodoro_estimate" type="number" value="<%= @todo.pomodoro_estimate %>">
    <input class="button add-new-todo-button" type="submit" value="Edit todo">
    <a href="/todo/index" class="simple-link">Go back...</a>
  </form>
</div>
```

The key thing to notice in the code above is the `value=` attribute in the two input fields. What we're doing here is pre-filling the input boxes with the information already associated with the todo we want to edit.

Now if you navigate to the /todo/edit/1 route, you should see the edit form with the todo information in the input fields!

Now, let's wire up the the edit button on the show page so we can click it and go to the edit form.

In the show.html.erb file we want to replace the following line:
```html.erb
<a href="#" class="button edit-todo-button">Edit</a>
```

with this line:
```html.erb
<a href="/todo/edit/<%= @todo.id %>" class="button edit-todo-button">Edit</a>
```

Now that we've successfully created the edit form, let's figure out how to get the updates entered in the form to actually save to the database.

## Update

### Route
Now you have to create the route the form above calls as an action. Add the following route to your routes file.
```ruby
get 'todo/update/:id', to: 'todo#update'
```

### Controller & Action
in your Todo controller, add the action below:
```ruby
def update
  t = Todo.find_by_id(params['id'])
  t.description = params['description']
  t.pomodoro_estimate = params['pomodoro_estimate']
  t.save
  redirect_to "/todo/show/#{t.id}"
end
```

Let's break down what is happening in each step above:
```ruby
t = Todo.find_by_id(params['id'])
```

Here we're finding the todo object we want to update in the Todo database and assigning it to the variable t.

```ruby
t.description = params['description']
```
We're taking the description of the todo and assigning the new content from the form to the todo.

```ruby
t.pomodoro_estimate = params['pomodoro_estimate']

```
We're taking the pomodoro_estimate of the todo and assigning the new value from the form to the todo.

```ruby
t.save
```
Here, we're saving the updated todo object to the database.

```ruby
redirect_to "/todo/show/#{t.id}"
```

### Setting the edit form action
Finally, we want to set the action attribute for the form so that the update action in the controller is triggered when we submit it. Enter the code below for the opening `<form>` tag:
```html.erb
<form action="/todo/update/<%= @todo.id %>">
```

After the Todo object has been updated, the action redirects to the todo's show page so we can see the changes.

Test it out to see if it works!

## Destroy
Finally, we want to be able to destroy todos that we don't want. The destroy action is much simpler than the others. We want to be able to click the destroy `<a></a>` link on the todo's show page. 

In the show.html.erb file we want to replace the following line:
```html.erb
<a href="#" class="button  delete-todo-button">Delete</a>
```

with this line:
```html.erb
<a href="/todo/destroy/<%= @todo.id %>" class="button delete-todo-button">Delete</a>
```

We still need the **RCA** flow.

### Route
We want to create a route for the destroy action. When Rails goes to this route, it will trigger the destroy action and then redirects to the index page again, since the show page for the deleted todo no longer exists.
```ruby
get 'todo/destroy/:id', to: 'todo#destroy'
```

We must use a dynamic route segment for this route as well, since Rails needs to know which todo we want deleted from the database.

### Controller & Action
In our controller, we now need an action. Define the destroy action in your Todo controller.
```ruby
def destroy
end
```

In our `destroy` action, we're going to create a variable `t`. In `t` we're going to store the Todo object that we want to delete. Then we are going to use the command `.destroy` to delete the todo from the database. Finally, since the show page for the todo doesn't exist anymore, we are going to redirect to the index page.
```ruby
def destroy
  t = Todo.find_by_id(params[:id])
  t.destroy
  redirect_to "/todo/index"
end
```

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add the edit, update, and destroy RCAV flows"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
