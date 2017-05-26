# Navigate Through the Command Line
So now that we have a general understanding of the command line let's learn how to do a few things.

The first thing we want to be able to do is to find our way around while we're in the command line. The CLI is made up of directories (what we call folders) and files. The whole set of directories that contain more directories and files is called the document tree. There are a few commands that we can use to easily figure out where we are in the document tree and get to where we want to go.

### `cd`
Let's start by going to our Cloud9 command line and typing in the following command:
```bash
$ cd
```
Hit enter after you are done.

Your prompt should now look something like:
```bash
username:~ $
```
`cd` stands for change directory, and it is the command we'll be using to navigate from one folder to another when we're in the command line.

### `pwd`
Before we can use the cd command to change our position, we need to know where we are and where we have the option of going. To get a bearing on your location in the file tree, enter the command
```bash
$ pwd
```
>Give your students a few seconds to enter in the pwd command.

```bash
/home/ubuntu
```

pwd stands for print working directory, and it will always return the path (or address) to the directory in which you are currently in. Based on what was returned just now, we are in a directory called Ubuntu, which is in a directory called home, which is in the root directory (or top most level folder) of the file tree.
