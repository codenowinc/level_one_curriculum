# Push Your Application to GitHub

## Initialize the repository with Git
Before you make any more changes to your Rails application, you should start tracking it with Git. Does anyone remember what Git is and why we use it?

>Give your students a moment to volunteer an answer. If no one volunteers, give a brief explanation of Git and what it is mainly used for.

So let's start tracking all of the changes we make to our code using Git. First, we tell Git that we want it to start tracking our app directory.

Enter the following command into the command line:
```Shell
$ git init
```

Next, you need to tell Git what files were changed and provide a brief description of the changes. Since this is the very first commit you are making for this application, all the files have changed since they are all new.

Enter the following two commands into the command line:
```Shell
$ git add -A
$ git commit -m “Initial commit”
```

Finally, you want to back your code up to the cloud, so you don't lose it, even if your Cloud9 workspace gets deleted or disappears for some reason. Remember that tab you had to leave open when you were setting up your GitHub repository? It's time to use it now.

Go to that tab and click the "Copy to clipboard" button on the right side of the page, under the **"...or push to an existing repository from the command line"** section.

```Shell
git remote add origin git@github.com:PUT_YOUR_LOGIN_HERE/YOUR_REPOSITORY_NAME.git
git push -u origin master
```


>Give your students a moment to do this. If someone accidentally closed the tab/window, instruct them to open a new tab, log back in to their GitHub account, and click on the todo_app repository in the sidebar.

Now go back to your Cloud9 workspace. Navigate to the command line, type ctrl + v and hit **enter**.

You have now connected your Rails application in Cloud9 to your todo_app GitHub repository. To make sure it worked, go back to the browser tab where you have GitHub open and refresh. You should now see your repository.

![Your Rails application in your GitHub repository](/images/push_your_application_to_github/02.png "Your Rails application in your GitHub repository")
