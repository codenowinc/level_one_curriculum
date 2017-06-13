# Install Ruby Gems and Postgres

## Locate the Gemfile
Now that you have created your Cloud9 workspace and first Rails application, there are a few housekeeping tasks that you need to take care of before you can start the application up.

In your file tree on the left side of the screen, locate the file named Gemfile and open it. The Gemfile is full of Ruby Gems which are pre-written Ruby programs and libraries in a self-contained format called a "gem". Gems provide functionality that many programmers need often. They allow programmers not to have to reinvent the wheel every time they start a new project.

>Give your students a moment to locate and open their Gemfile.
![Gemfile](/images/install_ruby_gems_and_postgres/01.png "Gemfile")

## Remove sqlite gem and add pg gem
There are a few changes you have to make in the Gemfile before you can install all of the Gems.

Remove the following code from lines 6 and 7.
```Ruby
# Use sqlite3 as the database for Active Record
gem 'sqlite3'
```

Add the following lines in its place
```Ruby
# Use Postgres as the database for Active Record
gem ‘pg’
```

Make sure to save by typing **ctrl + s**. You now need to enter a command into your command line to tell Rails to install these Ruby gems into the application.

>Make sure all of your students have correctly replaces the sqlite3 gem with the pg gem. It is imperative that they complete this step correctly. Otherwise, they will not be able to push their applications to Heroku.

Enter the following two commands into the command line, one at a time.
```Shell
$ bundle update
$ bundle install
```

Wait patiently after running the bundle install command. It may take a few minutes to complete.

## Set up the database.yml & Postgres database

In your file tree locate a file called database.yml. It will be located at todo_app/config/database.yml. Delete all the contents of your database.yml file and replace it with the code from the file I am going to share with you now.

>Share this [database.yml gist](https://gist.github.com/harshamurthy/7bdd2aa91d9232d591424794e6d8ce04 "database.yml") with your students.

Make sure to save the new contents of your database.yml file. Now you are going to enter in two commands in the command line that will set up your Postgres database and get it running.

>Make sure your students have properly replaced the stock database.yml contents with the contents found in the linked gist.

Enter the following two commands into the command line, one at a time:
```Shell
$ sudo service postgresql start
$ createdb todo_app_development
```

You have now successfully created and started up the Postgres database you will be storing all of your todo application's data in.
