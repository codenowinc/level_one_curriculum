# Make Your HTML Smart

Now that we have created our todo Index and Show pages in our Rails application, it's time to use some of the powers Rails gives us to make our HTML smart.

## The Objective
Our goal is to have a show page for every todo in our list, not just the first one. That seems simple enough! All we need to do is write the HTML for each todo's show page, just like we have done for the first todo in our lists. In the example todo application, we have seven todos in the list, so we'd need seven show pages. But wait, what happens when we add another todo to the list? We have to create a whole new file and write the HTML for that todo's show page? That's not very practical! Let's take a look at how to make our HTML smart so we can add as many todos to our lists as we want, and a show page is created for each one automatically. Better yet, let's do that with only one show.html.erb file!

## Embdedded Ruby
Take a look at the file name of your view files. Like we talked about earlier, you’ll notice they have the file extension .html.erb. We know that the .html extension designates that this file has HTML in it. Does anyone remember what the .erb extension stands for?

>Give your students a moment to volunteer an answer.

The .erb file extension stands for embedded Ruby. This indicates that the file can contain both HTML and Ruby code.

This is one of the most powerful abilities Rails gives you. You will be able to process logic in your HTML view files, and output the results of that logic to the screen the user sees in the browser.

Let’s see embedded Ruby in action! Before you can write Ruby code in your view file, you have to learn about embedded Ruby tags. Embedded Ruby tags are special characters that surround any Ruby code we write in the view file, so Rails knows how to differentiate between the HTML and the Ruby.

Here is what some embedded Ruby looks like in an html.erb file:
```html.erb
<h1>Example HTML Document with Ruby</h1>
<p>Let's do some math</p>
4 + 3 = <%= 4+3 %>
```

In the code block above, the code between the `<%= %>` tags is Ruby.

Now you try it! In your show.html.erb file, where you have the pomodoro estimate, replace it with `<%= 3+1 %>`.

Now return to your live app, and refresh the browser.

You should see the number 4 on the screen, even though we wrote an equation in the html.erb file.

So now we know how to make our HTML files "smart" with Ruby. But every time we want to create a new todo or change any information, we have to manually update the HTML code in the view file. This isn't how the apps you use everyday work.

When you sign up for a Facebook account, no one at Facebook is manually creating HTML files for all the pages in your account and hard coding all of your personal information and data.

Those pages are dynamically generated. Dynamic web pages and applications are ones that can automatically update as information keeps changing.

So what if we wanted a way to update the content that appears on our pages without actually changing any code in our HTML files?

## Instance Variables
One of the key tools we use to make view files dynamic is called the instance variable. Instance variables (you should remember what variables are from the Ruby tutorial you completed for homework) are variables that are defined in the controller file, and can be accessed from the associated view files. The catch is that the variable has to be defined in the action that corresponds to the view we want to access it in.

Here's an explicit example. If we wanted to use instance variables in our show.html.erb file, we would define them in the show action of our Todo controller.

Let's try it out.

In your show action in the Todo controller, enter the following code:
```ruby
@todo_description = "Make the curriculum"
@todo_pomodoro_estimate = 4
```

Your show action in your Todo controller should now look something like this:
```ruby
def show
  @todo_description = "Make the curriculum"
  @todo_pomodoro_estimate = 4
end
```

We have now defined two instance variables called todo_description and todo_pomodoro_estimate. Instance variables must have an `@` symbol in front of them to work. Without the `@` symbol, instance variables defined in the controller action won't be accessible in the view.

Now let's use these newly defined instance variables in our show.html.erb view file!

This is how the example show.html.erb file currently looks:
```html.erb
<h1>
  <img class="company-logo" src="https://public.3.basecamp.com/p/iahgNshn1oKq98sWGf1q89Vo/uploads/511042491/download/CodeNow%20Logo.png"></img>
  Workshop Todo List
</h1>

<div class="card">
  <input type="checkbox" name=""/>
  <h2>Make the curriculum</h2>
  <span class="pomodoro-estimate large-pomodoro-estimate"><%= 3+1 %> Pomodoros</span>
  <a href="#" class="button" id="edit-todo-button">Edit</a>
  <a href="#" class="button" id="delete-todo-button">Delete</a>
  <a href="/todo/index" class="simple-link">Go back...</a>
</div>
```

Let's replace the lines describing the todo and stating the Pomodoro estimate with our instance variables. Those two lines should now look something like this:
```html.erb
<h2><%= @todo_description %></h2>
<span class="pomodoro-estimate large-pomodoro-estimate"><%= @todo_pomodoro_estimate %> Pomodoros</span>
```

Now return to your live app, and refresh the browser. On your show page, you should see "Make the curriculum" for the todo description and "4" for the Pomodoro estimate! Go back to your Todo controller and change the data in one of your instance variables. Now refresh the page again and see if what's displayed on the page automatically changes.

Great! Now that we know how to use instance variables, we can begin on our quest to have a show page for every todo on our list, without writing another line of HTML!

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Define instance variables in Todo show action, and place in show view"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
