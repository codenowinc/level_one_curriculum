# Navigate Through the Command Line
So now that we have a general understanding of the command line let's learn how to do a few things.

The first thing we want to be able to do is to find our way around while we're in the command line. The CLI is made up of directories (what we call folders) and files. The whole set of directories that contain more directories and files is called the document tree. There are a few commands that we can use to easily figure out where we are in the document tree and get to where we want to go.

#### `cd`
  Let's start by going to our Cloud9 command line and typing in the following command:
  ```shell
  $ cd
  ```

  Hit enter after you are done.

  Your prompt should now look something like:
  ```shell
  username:~ $
  ```
  `cd` stands for change directory, and it is the command we'll be using to navigate from one folder to another when we're in the command line.

#### `pwd`
  Before we can use the `cd` command to change our position, we need to know where we are and where we have the option of going. To get a bearing on your location in the file tree, enter the following command:
  ```shell
  $ pwd
  ```
  >Give your students a few seconds to enter in the pwd command.

  You should see an output similar to the following:
  ```shell
  /home/ubuntu
  ```

  `pwd` stands for print working directory, and it will always return the path (or address) to the directory in which you are currently in. Based on what was returned just now, we are in a directory called ubuntu, which is inside of another directory called home, which is in the root directory (or top most level folder) of the file tree.

#### `ls`
  So now that we know where we are, we have to figure out where we can go. To see all the directories and files within the ubuntu directory that we're currently in, we use the following command:
  ```shell
  $ ls
  ```

  >Give your students a few seconds to enter the ls command.

  `ls` stands for list, and we use it to see what directories and files are in the directory we're currently in.

  After entering ls, you should see an output similar to the following:
  ```shell
  lib/  workspace/
  ```

  It looks like within the ubuntu directory, there are two directories named lib and workspace.

#### `cd` Again...
  Now that we know what our option are as far as where we can go, we can use the `cd` command followed by the name of the directory we want to change into.

  Enter the following command:
  ```shell
  $ cd workspace/
  ```

  >Give your students a few seconds to enter the `cd` workspace command

  After we `cd` into the workspace directory, we can immediately see that the prompt before the `$` in our command line has changed.

  Now that we've changed our location within the file tree let's take a moment to get our bearings. Enter the `pwd` command again.

  >Give your students a moment to enter the pwd command again. Ask them if they noticed what's different, and to explain what they noticed to the rest of the group. The path now reflects that they are in the workspace directory.
