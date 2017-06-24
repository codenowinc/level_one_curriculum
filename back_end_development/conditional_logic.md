# Conditional Logic
Conditional logic helps you make your application even smarter, by allowing you to instruct your application on how to make decisions.

Using conditional logic, you are going to tell your application how to send the correct todo's information to the show page, based on the URL the user enters in the URL bar.

The conditional logic will be written in your Todo Controller, in the show action. But before we write any code, let's plan out what we want to happen in detail.

## Pseudocode
Pseudocode is when we use plain language to describe what we want our code to do. This helps us plan out exactly what we want to happen, and understand the logic for how it's going to happen. We can then turn our pseudocode into actual code and see our plans executed step by step.

Here is what the pseudocode in the show action of the Todo Controller for the sample todo application would look:
```ruby
def show
  # If the user types in /todo/show/1 to the URL
  # make @todo_description equal "Make the curriculum"
  # and
  # make @todo_pomodoro_estimate equal "4"
  #
  # If the user types in /todo/show/2 to the URL
  # make @todo_description equal "Buy workshop supplies"
  # and
  # make @todo_pomodoro_estimate equal "3"
  #
  # If the user types in /todo/show/3 to the URL
  # make @todo_description equal "Meet with volunteer trainers"
  # and
  # make @todo_pomodoro_estimate equal "2"
  #
  # If the user types in /todo/show/4 to the URL
  # make @todo_description equal "Order food for Saturday and Sunday"
  # and
  # make @todo_pomodoro_estimate equal "1"
  #
  # If the user types in /todo/show/5 to the URL
  # make @todo_description equal "Check pre-work assignments"
  # and
  # make @todo_pomodoro_estimate equal "2"
  #
  # If the user types in /todo/show/6 to the URL
  # make @todo_description equal "Send workshop location to all the students"
  # and
  # make @todo_pomodoro_estimate equal "1"
  #
  # If the user types in /todo/show/7 to the URL
  # make @todo_description equal "Have a great workshop"
  # and
  # make @todo_pomodoro_estimate equal "0"
end
```

We have to write all of our pseudocode in comments because plain English will not compile in a Ruby file, and will cause an error.

Now that we have planned what we want to happen, let's write the code to make it real!

## If Statements
One of the most powerful features present in most programming languages is the ability to change the flow of the program as certain conditions change. The simplest form of flow control and logic in Ruby is called an "if statement".

These "if statements" check whether a condition is true or not. In Ruby they are created by writing the `if` keyword, followed by a condition and then the `end` keyword to end the statement. A basic if statement should look something like the following:
```ruby
if condition
  # Code to execute if 'condition' is true
end
```

From here the obvious question is: "How do we formulate a condition?" Well firstly, it's important to note that any expression that evaluates to a 'true' or 'false' value can be in the place of the condition. So the following would always output "Hello" as 'test_variable' will, in this case, always evaluate to true:
```ruby
test_variable = true

if test_variable
  puts "Hello"
end
```

"Real" conditions, for example comparing one variable to another, can be created by using 'conditional' or 'comparison' operators. These are operators that are made for comparing things, and when values are present at both sides of the operator, this will result in a 'true' or 'false' value. The basic conditional operators are:

### Conditional Operators
  * **`==`** - Is equal to
  * **`!=`** - Is not equal to
  * **`>`** - Is greater than
  * **`<`** - Is less than
  * **`>=`** - Is greater than or equal to
  * **`<=`** - Is less than or equal to

Let's put conditional logic and operators to the test by writing our first if statement. Navigate to the show action of your Todo controller.

>Give your students a moment to navigate to the right file.

First we'll create a variable that can store the id of a todo. Let's call it `todo_id` and set it's initial value equal to 1.
```ruby
def show
  todo_id = '1'
end
```

Now let's write our first if statement using the `todo_id` to write our condition.
```ruby
def show
  todo_id = '1'

  if todo_id == '1' # Remember, the `==` conditional operator is used to check if two things are equal to each other.
    @todo_description = "Make the curriculum"
    @todo_pomodoro_estimate = 4
  end
end
```

Now if you return to your live app and navigate to **/todo/show/1** you should see the show page for your first todo. But this is what we've been seeing the whole time. Let's write another if statement to really understand what is going on. Return to your Todo controller.

We can link multiple If statements together by using `elsif`. Look at the code below to see a demonstration:
```ruby
def show
  todo_id = '2'

  if todo_id == '1'
    @todo_description = "Make the curriculum"
    @todo_pomodoro_estimate = 4

  elsif todo_id == '2'
    @todo_description = "Buy workshop supplies"
    @todo_pomodoro_estimate = 3
  end
end
```

Set the value of `todo_id` to 2 and then return to your live app and navigate to **/todo/show/2**. You should now see the show page for your second todo! But what happens when you go to **/todo/show/1** now? It still displays the show page for the second todo. This is because our `todo_id` variable still has a value of 2 in the show action. We need the `todo_id` variable to get it's value from the number that is typed into the end of the URL, instead of setting it manually. If the user types **/todo/show/1** then `todo_id` should equal 1. If someone types **/todo/show/2** then `todo_id` should equal 2 and so on.

## The Params Hash
Luckily, Rails stores the information typed in to the URL in a handy place called the Params Hash. You should have learned about hashes in your homeowork. The name of the hash is params, and the name of the information is whatever we named the dynamic route segment in our routes file. In this case, we named our dynamic route segment `:id` as seen in our route: `get 'todo/show/:id', to: 'todo#show'`. So to access the dynamic route segment in the show action of our Todo controller, and set it as the value for our `todo_id` variable, we use the following code:
```ruby
def show
  todo_id = params[:id]
  ... # The ... signifies that there is more code in this section, but is not shown in the example for the sake of brevity
end
```

Add the above line of code to your show action. Now return to your live app and navigate to **/todo/show/1** and then **/todo/show/2**. You should now see the appropriate show pages for both todos!

Now see if you can add if statements to make the show pages for the rest of your existing todos work!

>Give your students some time to complete the rest of the if statements. As a bonus, see if your students can now add `<a></a>` tags to the todos on their index pages so that clicking the todo takes them to the appropriate show pages.

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add conditional logic if statements to the show action of the Todo controller"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
