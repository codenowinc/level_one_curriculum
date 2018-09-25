# Save and Push Your First Commit

## git `add` and `commit`
>Make sure the students have used the git init command to initialize their repository.

Now that we've initialized this directory to be tracked, we're ready to save the changes made to the repository up until this point. Because this is our first save, all of the contents in the repository will be treated as new changes. To stage all of the changes to be saved, we use the following command.
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

>Give your students a minute to use the git push command to push their code to GitHub.

Now that you've created your first commit and pushed your code to GitHub, log into your GitHub account and go to the GitHub repository you created earlier in the day. Within the repository, you should find the two HTML files you created in the previous Pomodoro.

Congratulations on pushing your first commit to GitHub! Tomorrow we'll be constantly saving the changes we make to our code and pushing to GitHub along the way. Get ready to follow this process over and over again!
