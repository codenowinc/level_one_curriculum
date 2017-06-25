# The Root Route
Currently when we go to the home page of our application, we see the default Ruby on Rails welcome page like the one below.

![Welcome aboard!](/images/the_root_route/01.png "Welcome aboard!")

When we want to navigate to our todo index page, we have to add /todo/index to the end of the URL. But Rails gives us a tool to set any page in our app to the home page. This page is called the root.

Let's make the /todo/index page the root of our application.

First, navigate to your routes.rb file. It should look similar to the code below.

***routes.rb file***
```ruby
Rails.application.routes.draw do
  get 'todo/index', to: 'todo#index'
  get 'todo/new', to: 'todo#new'
  get 'todo/create', to: 'todo#create'
  get 'todo/edit/:id', to: 'todo#edit'
  get 'todo/update/:id', to: 'todo#update'
  get 'todo/destroy/:id', to: 'todo#destroy'
  get 'todo/show/:id', to: 'todo#show'
end
```

Currently, when we add `'todo/index'` to the end of our URL we are taken to our list of todos. Instead, we want to see our list of todos on the home page of our application. To define our todo index page as our root route, we can replace `get 'todo/index', to: 'todo#index'` with the following code:

```ruby
root to: 'todo#index'
```

As you can see above, when defining the root route, we don't define the part that we add to the end of the URL. This is because the root route is always represented by a forward slash `/`.

The final step is to go through the various files in your app and change `todo/index` to `/`.

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add root route"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
