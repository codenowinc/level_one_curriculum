# Deploy to Heroku
Right now, your application is running locally. This means that your source code (the code your wrote to create the application) and the information you have saved in your database, only exists in Cloud9. Cloud9 stops running your application as soon as you close the browser window.

In order for your application to always be accessible to you and everyone else, you need to host your source code and database on a computer (server) that is always connected to the internet, and that can be accessed through a public URL.

In the old days, people had to set up their own infrastructure (servers and other hardware) to host their websites. Today, it's much easier. We use services that maintain this hardware for us. All we need to do is create an account, push our code to one of the servers, and sit back. (If your application is really popular, and has a lot of visitors, you'll need to pay to add more servers to handle the traffic, but that's a good problem to have!)

We're all going to use a service called Heroku to host our applications. You should have just created your Heroku account.

## Connect your Cloud9 workspace to your Heroku account
Now that you have a Heroku account let's connect your Cloud9 workspace to it. Cloud9 connects to Heroku in almost the same way that it connects to GitHub. To execute git commands on the command line, we always start the command with `git`. To execute Heroku commands on the command line, we'll use the command `heroku`.

Enter the following command into the command line.
```shell
$ heroku auth:login
```

Heroku will prompt you to enter the email and password associated with the account you just created. Make sure to enter them both carefully.

>Give your students a moment to enter their credentials.

After you authenticate Heroku in Cloud9, they should see a message in the terminal similar to the one below.

![Authenticating Heroku](/images/deploy_to_heroku/01.png "Authenticating Heroku")

## Create your first Heroku application from the command line
Now that your Heroku account is connected to your Cloud9 workspace let's create your first Heroku application.

_You must be in the root directory of your application for this next command to
work properly._ The root directory should be `~/workspace`.

Enter the following command into the command line replacing yourfirstname with your first name:
```shell
$ heroku create yourfirstname-todo-app
```

After entering the command, you  should see an output in the command line similar to the one below.

![Create a new Heroku application](/images/deploy_to_heroku/02.png "Create a new Heroku application")

## Push your Rails application to Heroku
You have a Heroku account, and you've created a Heroku app. Now it's time to push your Rails application up to its unique URL.

Enter the following command into the command line:
```shell
$ git push heroku master
```
Now that your code is added to heroku, lets set up your heroku data base with the todo table.
```shell
$ heroku run rake db:migrate
```
After the command finishes running (it may take a few moments) open a new browser tab and enter yourfirstname-todo-app.herokuapp.com in the URL bar to see your application live on the web! Now have the person sitting next to you pull it up on their computer!
