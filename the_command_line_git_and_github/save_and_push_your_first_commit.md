# Save and Push Your First Commit
Over the next three days, we're going to be writing a lot of code. You're going to want to save all of your hard work along the way. Sometimes, you'll want to rewind and go back to an older version of your code, maybe because you didn't like the direction you took it in.

To help with these version control and saving tasks, we use a program called Git, which is already installed in Cloud9. To start tracking the changes we make to our code, we must initialize the repository we're currently working in, telling it to use git.


## git `init`, `add`, and `commit`
To do this, first, we make sure we're in the correct directory. In our case, we want to be in the workspace directory. Using the correct terminal command, ensure that you are all in the correct directory.

>Give your students a moment to check their current working directory with pwd.

Now that we're sure we're where we want to be, we initialize the repo to use git by using the following command:
```shell
$ git init
```

This command stands for git initialize.

>Give you students a minute to use the git init command to initialize their repository.

Now that all the changes we make in this directory are being tracked, we're ready to save the changes made to the repository up until this point. Because this is our first save, all of the contents in the repository will be treated as new changes. To stage all of the changes to be saved, we use the following command.
```shell
$ git add -A
```

>Give you students a minute to use the git add command to stage their changes.

Before we can finalize the saving of our changes, we have to write a short description of the changes that are being saved. To do this we use the following command.
```shell
$ git commit -m "Initial commit"
```

The description of the changes goes in the quotes after -m. Because this is the first time we are committing or saving the changes, we describe it as the Initial commit.

>Give you students a minute to use the git commit command to describe their changes.


## Push to GitHub
The final step of this process is to push our code to GitHub. GitHub is an online platform where we can upload, save, share, and collaborate on code. To push to GitHub, use the following command.
```shell
$ git push -u
```

>Give you students a minute to use the git push command to push their code to GitHub.

Now that you've create your first commit, and pushed your code to GitHub, log into your GitHub account and go to the GitHub repository you created earlier in the day. Within the repository, you should find the two HTML files you created in the previous Pomodoro.

Congratulations on pushing your first commit to GitHub! Tomorrow we'll be constantly saving the changes we make to our code and pushing to GitHub along the way. Get ready to follow this process over and over again!
