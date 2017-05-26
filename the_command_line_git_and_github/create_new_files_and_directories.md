# Create New Files and Directories
Now that we've navigated to our workspace directory, we can learn to create new directories and files. To create a new directory in the command line we use the following command:
```shell
$ touch
```

followed by the name of the file, like this:
```shell
$ touch file_name.txt
```

Using the touch command, let's create a file named index.html.

>Give your students a moment to use the touch command to create a file named hello_world.html.

You'll notice that the hello_world.html file appeared in the file tree, inside the test directory, on the left of your screen. Double click the index.html file to open it in your text editor.

Enter the following code into your hello_world.html file.
```html
<h1>Hello world!</h1>
```

>Give your students a moment to open the hello_world.html file and enter in the single line of HTML.

You have just created your first HTML file! Now let's see how it looks in the browser. For us to see how this HTML looks when it is compiled by the browser, we need to run a server. Cloud9 makes this very easy.

Click the green arrow marked run at the top of your workspace. It will open up a server window in the same section as your command line at the bottom of the screen. Click the link that appears in the terminal window and select open.

Ta-da! The page you are now looking at is the compiled version of the HTML file you just created. You are looking at a static HTML page that you created! Go ahead and change hello world to something else and refresh the browser window. See what happens!

Let's go ahead and remove the hello_world.html file and test directory from our project.

Return to the command line tab and enter the following command:
```shell
$ rm hello_world.html
```

This will remove the hello_world.html file from the test directory. `rm` stands for remove.

>Give your students a moment to write the command to remove the hello_world.html file.

Now that we've removed the file let's remove the test directory. There's one catch, you can't delete a directory while you're still in it. We have to navigate one level up to the directory which contains the test directory that we created. To traverse to the previous directory we use a command we're familiar with, `cd`.

```shell
$ cd ..
```

Now if you look at your location by using `pwd`, you should see an output similar to the following:
```shell
/home/ubuntu/workspace
```

Type `ls` to see a list of all the directories and files within the directory you are currently located in, workspace.

To delete a directory, we use a slightly different command, `rmdir`.
```shell
$ rmdir directory_name
```

>Give your students a moment to navigate back to the workspace directory, and then try the command to delete their test directory.

Now that we understand how to create and remove directories and files, let's create the files we're going to need to create our static HTML & CSS mockups of the sketches you drew earlier.

We want to create two HTML files. One called index.html and another called show.html. Using the commands you just learned, can you create those two HTML files?

>Give your students a few minutes to create these new html files using the `touch` command. Help them get the answer by questioning their thought process, if they are going off track.

We also want to create two CSS files. One called index.css and another called show.css.

>Give your students a few minutes to create these new css files using the `touch` command.
