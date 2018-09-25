# Create Files In the Command Line
Now that we've navigated to our workspace directory, we can learn to create new directories and files. To create a new file in the command line we use the following command:
```shell
$ touch
```

followed by the name of the file, like this:
```shell
$ touch file_name.txt
```

## Create Your First HTML File
Using the touch command, let's create a file named index.html.

>Give your students a moment to use the touch command to create a file named index.html.

You'll notice that the index.html file appeared in the file tree, inside the todo_app_front_end directory, on the left side of your screen. Double click the index.html file to open it in your text editor.

Enter the following code into your index.html file.
```html
<h1>Hello world!</h1>
```

>Give your students a moment to open the index.html file and enter in the single line of HTML.

You have just created your first HTML file! Now let's see how it looks in the browser. For us to see how this HTML looks when it is compiled by the browser, we need to run a server. Cloud9 makes this very easy.

Click the green arrow marked run at the top of your workspace. It will open up a server window in the same section as your command line at the bottom of the screen. Click the link that appears in the terminal window and select open.

Ta-da! The page you are now looking at is the compiled version of the HTML file you just created. You are looking at a static HTML page that you created! Go ahead and change "Hello world!" to something else and refresh the browser window. See what happens!

## A Few More Files You'll Need
Now that we understand how to create files, let's create the files we're going to need to create our static HTML & CSS mockups of the sketches you drew earlier.

We've already created the first HTML file we'll need, index.html. The second HTML file we'll need is called show.html. Using the commands you just learned, can you create show.html?

>Give your students a minute to create this HTML file using the `touch` command. Help them get the answer by questioning their thought process, if they are going off track.

We also want to create two CSS files. One called index.css and another called show.css. We'll learn what CSS is tomorrow!

>Give your students a few minutes to create these new css files using the `touch` command.
