# Routes, Controllers, Actions, and Views

The first thing we want to do is import the HTML and CSS from weekend one into our new Rails applications. But with a rails application, getting your content and styles to display in the browser isn't as simple as executing your HTML file. Rails has many parts that must work together.

To start, lets get a high-level overview of how a Rails applications work. The following four letters are going to be very important. **R C A V** These pieces are the foundation for everything that will come next.

##R for Route
A route is what the user types in to the URL bar at the top of the browser (We use routes in a few other places as well, but this is the main function for where we are starting). Think of your routes file as the reception desk for the rest of your app. It handles incoming requests and sends them to the right place.

![Routes](/images/routes_controllers_actions_views/01.png "Routes")

You can find your routes.rb file at ***config/routes.rb***. Go ahead and open your routes file now.

>Give your students a moment to open their routes.rb file.

##C for Controller
A controller is the logical center of your application. It coordinates the interaction between the user, the views, and the model. You'll learn about views and models shortly. The controller is also a home to a number of important ancillary services. The routes file takes requests and directs them to the appropriate controller.

![Controllers](/images/routes_controllers_actions_views/02.png "Controllers")

Rails applications can have multiple controllers. Usually a controller is made to handle all of the behaviors around a single resource in the application. In our case, we will have a controller that handles all of the logic around a todo.

All Rails applications come with one controller by default: the Application Controller. You can find your application_controller.rb at ***app/controllers/application_controller.rb***. When we create a controller for todos, it will be saved in the ***controllers*** directory.

##A for Action
