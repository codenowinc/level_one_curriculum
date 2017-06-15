# Routes, Controllers, Actions, and Views

The first thing we want to do is import the HTML and CSS from weekend one into our new Rails applications. But with a rails application, getting your content and styles to display in the browser isn't as simple as executing your HTML file. Rails has many parts that must work together.

To start, lets get a high-level overview of how a Rails applications work. The following four letters are going to be very important. **RCAV** These pieces are the foundation for everything that will come next.

## R for Route
A route is what the user types in to the URL bar at the top of the browser (We use routes in a few other places as well, but this is the main function for where we are starting). Think of your routes file as the reception desk for the rest of your app. It handles incoming requests and sends them to the right place.

![Routes](/images/routes_controllers_actions_views/01.png "Routes")

You can find your routes.rb file at ***config/routes.rb***. Go ahead and open your routes file now.

>Give your students a moment to open their routes.rb file.

## C for Controller
A controller is the logical center of your application. It coordinates the interaction between the user, the views, and the model. You'll learn about views and models shortly. The controller is also a home to a number of important ancillary services. The routes file takes requests and directs them to the appropriate controller.

In the image above, under the R is the example of the route we will put in our routes.rb file. `get 'todo/index', to: todo#index`. In the `todo#index` part of the route, the first word, `todo`, refers to the controller the route points to. In this case, our example route is pointing to a controller called todo. Illustrated in the image below. The `index` in the `todo#index` portion of the route refers to the specific action within the controller the route is pointing to. We will learn more about actions in the next section.

![Controllers](/images/routes_controllers_actions_views/02.png "Controllers")

Rails applications can have multiple controllers. Usually a controller is made to handle all of the behaviors around a single resource in the application. In our case, we will have a controller that handles all of the logic around a todo. This controller will be called todo_controller.rb.

All Rails applications come with one controller by default: the Application Controller. You can find your application_controller.rb at ***app/controllers/application_controller.rb***. When we create a controller for todos, it will be saved in the ***controllers*** directory.

## A for Action
When a Rails application receives a request, the routes file will determine which controller to send the route too, but it also determines which action within the controller to run. This means that our controllers are filled with actions that will be run depending on the request made to the Routes file.

![Actions](/images/routes_controllers_actions_views/03.png "Actions")

The name of the action corresponds to the second part of the route. In this case, our route is `todo#index`, our controller name is `todo_controller`, and our action name is `index`. Get the pattern?

## V for View
The final part of the **RCAV** flow is the view. The view file is where the content and HTML you want the user to see is located.

![Views](/images/routes_controllers_actions_views/04.png "Views")

Rails applications can have many view files. In the first weekend of the workshop, you made two views for todos, the index view and the show view. Rails follows a convention to make sure that views are properly linked to the controllers and actions they belong to. In your file tree, navigate to the ***app/views*** directory. In it you will see a directory named layouts. Eventually we will create another directory in the views directory named todo. Then within the todo directory, we will have a separate html.erb file that corresponds to each action within our todo_controller. So within the views directory, we have a a directory named after the controller (todo), and a file named after the action (index).

## Review
That was a lot of information to cover, but don't worry if you don't understand everything. We'll go through the **RCAV** process step by step, and add your index page to your Rails application in the next section.

![RCAV Recap](/images/routes_controllers_actions_views/05.png "RCAV Recap")
