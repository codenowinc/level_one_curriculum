# Create Your First Database Table

## A Place to Store Your Data
Databases take on the task of storing and organizing large amounts of information, so we don’t have to do it ourselves in our applications.

So if we want to get rid of the repeated instance variables in the show action of our controller, we can store that information in a database instead.

We can set up the database through our command line. The first step is creating an object called a Todo in our app. It is instances of this Todo object that will be saved in the database. Objects are represented in Rails through what are called models. We are going to create the Todo model in our app now.

## Generate Your First Model
As we know, Rails gives us many tools. One of these tools is a set of generators that developers can use to have Rails automatically set up files and directories for them. One of these generators is a Model generator. We'll use the following command to set up the Todo model:
```shell
$ rails generate model Todo description:string, pomodoro_estimate:integer, complete:boolean
```

After you run the command, you’ll see that rails generated a couple of different files for us. The migration file, and the model file.

![Migration and Model File](/images/create_your_first_database_table/01.png "Migration and Model File")

Let’s look at the migration file first located at ***db/migrate/last_migration_file***.

>Give your students a moment to navigate to their migration file.

![Last Migration File](/images/create_your_first_database_table/02.png "Last Migration File")

What this migration is doing, is setting up a table inside your new database. You can think of a table kind of like a spreadsheet. This migration file is setting up a table named Todos.

![Todo Data Model](/images/create_your_first_database_table/03.png "Todo Data Model")

The other file that was created is a model file ***located at app/models/todo.rb***. The model file is a container for all the code that is related to a particular object. Right now this file looks empty, but at the top, there is a `Class Todo < ActiveRecord::Base`.

![Todo Model](/images/create_your_first_database_table/04.png "Todo Model")

The < ActiveRecord::Base is our Todo model inheriting code directly from Rails, allowing the model to connect to the database table that we are about to create using the migration file we just looked at.

To run the migration file, we have to go through two steps. First, enter the following command:
```shell
$ bundle install
```

Then enter the migration command:
```shell
$ rake db:migrate
```

What this does is it runs the migration file to set up the database table. The migration file isn’t the actual database; it’s just instructions for setting up the database.

After you run `$ rake db:migrate`, you will see an output in your console like the one pictured here indicating that the lists table was created.

![Lists Table Created](/images/create_your_first_database_table/05.png "Lists Table Created")

Now that we’ve created our database for lists, how do we store information in our database?

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add list model and migration file"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
