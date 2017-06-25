# Pull Request Activity

## Fork the repository
Fork [this repository](https://github.com/CodeNowOrg/student_profiles "Student Profiles") to your GitHub account by clicking the "Fork" button in the top right corner of the page.

A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project. Most commonly, forks are used to either propose changes to someone else's project or to use someone else's project as a starting point for your own idea.

You can use forks to propose changes for bug fixes. Rather than logging an issue for a bug you've found in someone's code, you can:

* Fork the repository.
* Make the fix.
* Submit a pull request to the project owner.

If the project owner likes your work, they might pull your fix into the original repository!

## Clone the code into Cloud9 and create your workspace
Close any existing Cloud9 workspaces you have open. We're going to create a new Cloud9 workspace from the GitHub repository you just forked. Return to your Cloud9 dashboard and click the plus button. You should end up on a page that looks like the one below.

![New Cloud9 Workspace](/images/pull_request_activity/01.png "New Cloud9 Workspace")

Now navigate back to your newly forked repository in GitHub. You're going to click the green button on the right side of the page that says "clone or download".

![Clone or Download](/images/pull_request_activity/02.png "Clone or Download")

Making sure it's set to SSH, click the clipboard on the right side of the URL in the box that opens when you click "clone or download".

![Copy to your Clipboard](/images/pull_request_activity/03.png "Copy to your Clipboard")

Now that you've copied the URL to your newly cloned repository, return to your new Cloud9 workspace tab and paste it into the secion titled "Clone from Git or Mercurial URL (optional)". Don't forget to name your workspace something descriptive.

![Clone from Git or Mercurial URL (optional)](/images/pull_request_activity/04.png "Clone from Git or Mercurial URL (optional)")

Select the Ruby on Rails workspace tile, and click "Create workspace".

## RCAV flow for your profile page
You should have a newly minted workspace that looks like the screen below.

![Cloud9 Workspace](/images/pull_request_activity/05.png "Cloud9 Workspace")

The goal is to create a profile page for yourself. Go through the **RCAV** flow and create an show page that displays your name, favorite restaurant, favorite tv show, and a short 5 sentence bio about yourself. Use instance variables to store the data and display it on your show page. Your show page should look something like the page below:

![Example profile page](/images/pull_request_activity/06.png "Example profile page")

## Commit your changes and push to your forked repository
Now that you have created your profile page, it's time to commit and push your changes to your forked repository on GitHub.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add my profile page"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.

## Submit a pull request on GitHub
Pull requests let you tell others about changes you've pushed to a GitHub repository. Once a pull request is sent, interested parties can review the set of changes, discuss potential modifications, and even push follow-up commits if necessary. Now you're going to submit a pull request to get your profile added to the original codebase.

Navigate to your forked repository on GitHub and click the "New pull request" button.

![New pull request](/images/pull_request_activity/07.png "New pull request")

You will be taken to a page that shows all the changes between the original code and your new code.

![Changes](/images/pull_request_activity/08.png "Changes")

Click "Create pull request". You will be taken to a page titled "Open a pull request". There will be an automatically generated commit message based on the commit message you entered when you pushed your code to your forked repository a few steps earlier.

![Changes](/images/pull_request_activity/09.png "Changes")

Go ahead and click "Create pull request". GitHub will check if there are any conflicts between your code and the code that you are trying merge your code into. After you created your request, the owner of the original repository will have to approve it before your code gets merged in.

We'll go through everyone's pull requests together as a class and merge them in to the original code base.
