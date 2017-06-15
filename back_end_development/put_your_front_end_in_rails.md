# Put Your Front End In Rails
Now that we have gone over the **RCAV** flow, let's put it into practice. Our goal is to get our index.html view from weekend one to run in our Rails application. All we need to do is follow the **RCAV** flow!

Before we start, let's start our servers and run our Rails applications, so we can see our changes happen as we make them. Click the "Run project" button in the menu bar. A new window will open in your terminal, at the top, you a link will appear. Click the link and select "Open". You should have a new tab open that looks like the image below.

![New Rails Application](/images/put_your_front_end_in_rails/01.png "New Rails Application")

## Step One - Route
Navigate to ***cofig/routes.rb***. In your routes file, you will see a wall of grayed out text. This is helpful information Rails has provided developers about how to use the routes file. For now, we don't need to worry about this information. We can delete it. Remove all of the lines that start with a `#` between the `Rails.application.routes.draw do` and `end`.

>Give your students a moment to clear the comments out of their routes file.

Your routes.rb file should now have two lines of code.
```Ruby
Rails.application.routes.draw do
end
```

Now we want to write our first route. We want the user to be able to add **/todo/index** to the end of our app's URL and be taken to a page that shows our todo lists. Let's see what happens when we add **/todo/index** to the end of our application's route in the URL bar like the image below.

![/todo/index](/images/put_your_front_end_in_rails/02.png "/todo/index")

You will see an error screen telling us that there is no route matching [GET] "/todo/index".

![No Route](/images/put_your_front_end_in_rails/03.png "No Route")

Let's add our route now! In your routes.rb file, add the following code:
```Ruby
get 'todo/index', to: 'todo#index'
```

Here is what this route is telling our Rails application to do:
When the user adds /todo/index to the URL, direct the application to a controller named Todo, and an action named index within the Todo controller. Process the code in the index action, and got to a directory named views. With the views directory, find a directory named after the controller, in this case todo. Within the todo directory, find an html.erb file named after the action, in this case, index. Display the index.html.erb file to the user in the browser.

Now return to your live app, and refresh the browser. You should see an error screen like the one below.

![No Controller](/images/put_your_front_end_in_rails/04.png "No Controller")

This error screen is telling us that the route is trying to access a controller that doesn't exist yet. So let's create it!
