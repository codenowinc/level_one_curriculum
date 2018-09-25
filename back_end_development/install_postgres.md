# Install Postgres
Just like there are many different programming languages (Ruby, Java, C, Python, etc.), there are multiple database languages that programmers use to create and maintain databases. Rails comes with a database language called SQLite by default, but we're going to change our apps to use a database language called PostGres or PG for short. We do this so we can host our applications using a service called Heroku, which you all will get to know later on.

## Locate the Gemfile
In your file tree on the left side of the screen, locate the file named Gemfile and open it. The Gemfile is full of Ruby Gems which are pre-written Ruby programs and libraries in a self-contained format called a "gem". Gems provide functionality that many programmers often need and use. They allow programmers not to have to reinvent the wheel every time they start a new project.

>Give your students a moment to locate and open their Gemfile.
![Gemfile](/images/install_postgres/01.png "Gemfile")

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
gem 'pg', '~> 0.11'
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

>Share this [database.yml gist](https://gist.githubusercontent.com/harshamurthy/7bdd2aa91d9232d591424794e6d8ce04/raw/dfb421e2184a3eaae3536a2bb2e3b931bcc84a98/database.yml "database.yml") with your students.

Make sure to save the new contents of your database.yml file. Now you are going to enter in two commands in the command line that will set up your Postgres database and get it running.

>Make sure your students have properly replaced the stock database.yml contents with the contents found in the linked gist, keeping the same exact text alignment/tabs.

Enter the following two commands into the command line, one at a time:
```Shell
$ sudo service postgresql start
$ createdb todo_app_back_end_development
```

You have now successfully created and started up the Postgres database where you will be storing all of your todo application's data!

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Install postgres and update database.yml"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
