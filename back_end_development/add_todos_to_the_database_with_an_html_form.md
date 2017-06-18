# Add Todos to the Database With An HTML Form

## **CRUD** and the Golden Seven Actions
**CRUD** is an acronym used to summarize the basic actions a user would want to take on an object in the database.

**CRUD** stands for:
1. Create
2. Read
3. Update
4. Destroy

Let's demonstrate **CRUD** with an example. When a user come to the todo list app, they should be able to do some basic things. They should be able to **Create** a todo. They should be able to **Read** or see the show page of the individual todo they just created. They should be able to **Update** the todo. And finally, they should be able to **Destroy** or delete the todo. It's a fairly straightforward concept.

Now each of these actions that the user should be able to take, has to map over to a specific **RCAV** flow in our application. Remember, everything always comes back to **RCAV**. The **CRUD** capabilities map over to seven distinct actions in our controller. We already have two of them done, index and show! Here's a breakdown on all seven golden actions. They are called the golden seven because they are used almost universally in every database backed application.

**The Golden Seven Actions**
1. New
2. Create
3. Edit
4. Update
5. Show
6. Index
7. Destroy

Now each one of these actions is part of an entire **RCAV** flow, meaning they each need a route, controller, action, and view. In our case, because all of these actions are associated with todos, they'll all be located in the Todo Controller.

Let's take a look at what each action is supposed to do:
The **New** action will display a page with a form to enter in the information for a new todo.
The **Create** action will take what the user entered in the new form, and save that information to the database.
The **Edit** action will display a page with a form to edit the information of an existing todo.
The **Update** action will take the new information the user entered in the edit form, and save that information to the database.
The **Show** action will display a page with the information for one specific todo. We already have the show action!
The **Index** action will display a page with a list of all the todos in the database. We already have the index actions!
The **Destroy** action will allow the user to delete a specific todo from the database.

Now that we have a general understanding of the **CRUD** structure and the Golden Seven Actions, let's get started on allowing users to add Todos to the database using the **New** and **Create** actions!

## New
We can get information into our database using the command line as developers, but we can’t expect people using our applications to do that. It would be a lot better if users could see a form and use it to enter their information into the database. Let’s talk about HTML forms and how we can use them.

Every form in a Rails application needs two actions in the controller. One to display the actual form (The new action), and one to save the information once the form has been filled out (the Create action).

And as we know, any time we need to create a new action, we start from the top of the **RCAV** process.

### Route
In the routes file, create the following route above the `'todo/show/:id', to: 'todo#show'` route. It is very important to add this route above the route with the dynamic route segment.
```ruby
get 'todo/new', to: 'todo#new'
```

This route will take the user to a page that displays the HTML form where they can enter enter the information for the new todo they want to add to the database.

### Controller & Action
Now let’s go to the Todo controller and create our 'new' action.
```ruby
def new
end
```

### View
Finally, we create a view file named new.html.erb in the ***app/views/todo*** directory. In this view file, insert the following HTML:
```html.erb
<h2>Add a new todo...</h2>

<form action="#">
  <input class="text-input" id="new-todo-description" name="description" type="text" placeholder="Add a new todo...">
  <input class="text-input" id="new-pomodoro-estimate" name="pomodoro-estimate" type="number" placeholder="Pomodoro estimate...">
  <input class="button" id="add-new-todo-button" type="submit" value="Add todo">
</form>
```
As you can see in this HTML code, there is a form tag. The form tag has an attribute called action. This action accepts a route. This is the route that gets executed when a user clicks the submit button on the form.

Run your local server and navigate to /todo/new. You will see the new form!

## Create
Now that we've completed the **RCAV** flow for the new action which displays the form, it's time to complete the **RCAV** flow for the create action which saves the information from the form to the database.

### Route
Add the following route to your routes.rb file, under your route for the new action.
```ruby
get 'todo/create', to: 'todo#create'
```

### Controller & Actions
After the route comes the controller and action. Head over to Todo Controller and add the following action.
```ruby
def create
end
```

This time though, we're actually going to enter some Ruby code into our action instead of leaving it blank. The purpose of the create action is to take the data you just entered into the form in the browser and save it to the database.

We can write the Ruby code we used in the Rails console to add todos to the database. Except this time, we'll only have to write it once.

Enter the following code in your create action:
```Ruby
def create
  t = Todo.new
  t.description = params['description']
  t.pomodoro_estimate = params['pomodoro_estimate']
  t.save
  redirect_to "/todo/show/#{ t.id }"
end
```

Let's break down what just happened.

```ruby
t = Todo.new
```
In this line, you are creating a new Todo object in your database and assigning to a variable t.

```ruby
t.description = params['description']
```
The params hash is where Rails automatically stores all the information a user enters in the browser, whether that's in the URL bar on in a form. We know to call the piece of information 'description' because when we wrote the HTML for the form, that's what we called it in the name attribute!

![Naming the Input](/images/add_todos_to_the_database_with_an_html_form/02.png "Naming the Input")

Because we named the name attribute escription in the HTML of the form, we can refer to the data that the user inputs into the field as new-todo-description from the Params hash.

```ruby
t.description = params['pomodoro_estimate']
```
The params hash is where Rails automatically stores all the information a user enters in the browser, whether that's in the URL bar on in a form. We know to call the piece of information 'description' because when we wrote the HTML for the form, that's what we called it!

```ruby
t.save
```
This line saves the todo to the database. If we don't save, then the new Todo object that was created won't get stored in the database and will disappear into the ether!

```ruby
redirect_to "/todo/show/#{ t.id }"
```
Here's a line we haven't seen before! If you noticed, we haven't created a view for the create action that we just wrote in the todo controller. Can anyone take a guess as to why we haven't made a view for this action?

The purpose of the create action is to save the information the user enters into the form in the database. In this case, the user is creating a new todo. After a new todo is saved to the database, it automatically gets assigned an id by Rails, and we want to show the new todo to the user. So `redirect_to "/todo/show/#{ t.id }"` goes to the show route followed by the number associated with this new todo.

### Updating the New form
Now that we have the **RCAV** flow set up for create, let's add the route to our form action attribute in the new.html.erb file so the information entered in the form gets saved to the database.

Your opening `<form>` tag in your new.html.erb file should look like the code below.
```html.erb
<form action="/todo/create">
...
```

Now got to your live application and navigate to the /todo/new route. Enter in the information for a new todo and hit submit. You should be taken to the show page for the todo you just created!

Now that we know how to create new todo objects with a form, it's time to learn how to edit, update, and delete todos!

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add the RCAV flows for the new and create actions"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
