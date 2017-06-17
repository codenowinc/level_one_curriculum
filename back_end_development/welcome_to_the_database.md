# Welcome to the Database
Let's take a look at what we've done so far.
1. We created a new Rails application and learned about the file and directory structure that Rails gives us out of the box.
2. We created a new GitHub repo, initialized our Rails application to be tracked by Git, and pushed our new code up to GitHub.
3. We learned about the **RCAV** flow, and how it is the bedrock of all Rails applications.
4. We completed the **RCAV** flow for our index and show pages and imported our HTML and CSS from weekend one into our new applications.
5. We made our HTML files intelligent by learning to add embedded Ruby.
6. We **DRY**ed up our code by using dynamic route segments to create a show page for every todo without adding more view files.
7. We used conditional logic to display the right show page for the right route.
8. Finally, we linked each show page to the correct todo on the index page.

In the summary above, you'll notice the term **DRY** in step six. **DRY** stands for **Don't Repeat Yourself** and it's one of the core tenets of programming. Programmers are lazy, and we always want to write as little code as possible. So far, we've done a good job of avoiding repetition. One example of staying DRY is using the same show view file to display every todo's show page.

But it looks like we're still repeating ourselves quite a bit in the show action of the todo controller. Every time we add a new todo to our list, we'll have to add another `ifelse` statement to our action. This isn't very practical! Imagine if someone at Facebook or Instagram had to write some code every time a new user signed up or someone posted a photo. They wouldn't be able to keep up!

Luckily, we can use databases to handle the burden of information.

A database is a collection of information that is organized so that it can be easily accessed, managed and updated.

Data is organized into rows, columns and tables, and it is indexed to make it easier to find relevant information. Data gets updated, expanded and deleted as new information is added.

Let's create our first database!
