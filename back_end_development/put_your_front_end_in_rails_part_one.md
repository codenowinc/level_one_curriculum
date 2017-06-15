# Put Your Front End In Rails - Part One
Now that we have gone over the **RCAV** flow, let's put it into practice. Our goal is to get our index.html view from weekend one to run in our Rails application. All we need to do is follow the **RCAV** flow!

Before we start, let's start our servers and run our Rails applications, so we can see our changes happen as we make them. Click the "Run project" button in the menu bar. A new window will open in your terminal, at the top, you a link will appear. Click the link and select "Open". You should have a new tab open that looks like the image below.

![New Rails Application](/images/put_your_front_end_in_rails_part_one/01.png "New Rails Application")

## Step One - Route
Navigate to ***cofig/routes.rb***. In your routes file, you will see a wall of grayed out text. This is helpful information Rails has provided developers about how to use the routes file. For now, we don't need to worry about this information. We can delete it. Remove all of the lines that start with a `#` between the `Rails.application.routes.draw do` and `end`.

>Give your students a moment to clear the comments out of their routes file.

Your routes.rb file should now have two lines of code.
```Ruby
Rails.application.routes.draw do
end
```

Now we want to write our first route. We want the user to be able to add **/todo/index** to the end of our app's URL and be taken to a page that shows our todo lists. Let's see what happens when we add **/todo/index** to the end of our application's route in the URL bar like the image below.

![/todo/index](/images/put_your_front_end_in_rails_part_one/02.png "/todo/index")

You will see an error screen telling us that there is no route matching [GET] "/todo/index".

![Missing Route](/images/put_your_front_end_in_rails_part_one/03.png "Missing Route")

Let's add our route now! In your routes.rb file, add the following code:
```Ruby
get 'todo/index', to: 'todo#index'
```

Here is what this route is telling our Rails application to do:
When the user adds /todo/index to the URL, direct the application to a controller named Todo, and an action named index within the Todo controller. Process the code in the index action, and got to a directory named views. With the views directory, find a directory named after the controller, in this case todo. Within the todo directory, find an html.erb file named after the action, in this case, index. Display the index.html.erb file to the user in the browser.

Now return to your live app, and refresh the browser. You should see an error screen like the one below.

![Missing Controller](/images/put_your_front_end_in_rails_part_one/04.png "Missing Controller")

This error screen is telling us that the route is trying to access a controller that doesn't exist yet. So let's create it!

## Step Two - Controller
Based on the error screen above, we know the next step is to create the Todo controller. As we discussed in the previous section, all controllers go in the ***app/controllers*** diretory. Navigate to the directory in your file tree.

>Give your students a moment to navigate to the controllers directory in their file tree.

In this directory, we are going to create a controller called **todo_controller.rb**. Controller files follow a naming convention called snake case, meaning all words in the title are lower case and separated by a underscore. Right click the ***controllers*** directory and select "New File".

>Give your students a moment to create their new todo_contrller.rb file. Make sure they have saved it in the correct repository.

In your new todo_controller.rb file, enter the following code:
```Ruby
class TodoController < ApplicationController
end
```

Now return to your live app, and refresh the browser. It seems that the application is no longer having trouble finding the Todo Controller! But we do have a new error on the screen. The action 'index' could not be found for TodoController

![Missing Action](/images/put_your_front_end_in_rails_part_one/05.png "Missing Action")

Can anyone take a guess at what this error means?

## Step Three - Action
It means we don't have an action called index in our Todo Controller. So we have to create that as well! Do you see the pattern forming here?

Inside your Todo Controller, add the following code so your controller file looks like the code below:
```Ruby
class TodoController < ApplicationController
  def index
  end
end
```

Currently, we can leave our index action empty since we don't want any logic to be executed on our view page. We'll add some Ruby code to it later!

Now return to your live app, and refresh the browser. Yet another different error! What does it say this time?

![Missing Template](/images/put_your_front_end_in_rails_part_one/06.png "Missing Template")

In Rails, templates and views are used interchangeably. It looks like we're missing the last piece to our **RCAV** flow! All we have to do is add our view template!

## Step Four - View Template
As mentioned previously, there is a directory in your file tree called views. It can be found at ***app/views***. In order for our view template to display properly we have to follow the correct naming and organizing convention. Right click the views directory in your file tree and select "New Folder".

Name the folder after the Controller it is connected to - **todo**. Now right click your newly created todo directory and select "New File". Name the file after the Action it is connected to - **index.html.erb**. You may notice that your view file has two file extensions: .html is for HTML of course. But what is .erb? **.erb** stands for embedded Ruby, and it is one of the superpowers given to us by the Rails framework. We can embed Ruby code into our HTML documents to make them smart!

After you have created the todo directory and the index.html.erb file, return to your live app and refresh the browser. No errors!

## Write HTML
Return to your index.html.erb file and write some HTML.
```HTML
<h1>Hello world!</h1>
```
Now go back to you live app and refresh the page. You should see your HTML displayed on the screen! We have successfully completed the **RCAV** flow.

![HTML!](/images/put_your_front_end_in_rails_part_one/07.png "HTML!")

Now we can start moving our front end HTML and CSS from weekend one to our Rails applications. But first...

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Complete RCAV flow for Todo Index"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
