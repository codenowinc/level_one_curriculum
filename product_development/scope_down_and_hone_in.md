# Scope Down and Hone In

### ***[Keynote](https://www.dropbox.com/s/j1u6i9fugh9dyoj/04%20-%20Keynote%20-%20Scope%20Down%20and%20Hone%20In.key?dl=0 "Scope Down and Hone In - Keynote") | [PowerPoint](https://www.dropbox.com/s/15y7287fxrinsj8/04%20-%20PowerPoint%20-%20Scope%20Down%20and%20Hone%20In.pptx?dl=0 "Scope Down and Hone In - PowePoint")***

Now it's time to drill a little deeper. We'll take the most important feature of our PomoDoro app, tracking assignments, and list out all the functionality we'll need to make the feature work.

It's important to list out the functionality of a feature in detail. Initially, a feature can seem very simple, but if you dig deeper, there are several moving parts that come together to make a feature work properly.

Let's look at what Instagram's most important feature, posting photos, looks like when we break down its functionality.

The following are all the affordances a user is given for posting a new photo to their Instagram account. Even though posting a photo seems simple on the surface, there are many things that need to be laid out to fully understand how the feature is going to get built.

### Post a Photo - Instagram
  * Choose photo source (Phone library, Take photo, Take video)
  * Apply filter
  * Edit photo
  * Write caption
  * Tag people
  * Add location
  * Cross post to other social media accounts

Note how posting a photo can involve taking a new photo or video from within the app itself. They have also provided me with the option to cancel the post, select multiple pictures, create a layout, and change the size of the photo.

Now it's time to wrap our heads around where we're going to start building. We've decided that the recording an assignment feature is the most impactful place to start building our app. Let's list out the affordances this feature is going to provide the user.

Before we can think about the different parts of this feature, we have to think about the different pieces that make up a todo.

First, we have to determine what pieces of information make up an to-do.

### Anatomy of a todo
  * a description of what needs to get done
  * an estimate of the number of Pomodoros it will take to complete
  * a status indicating if it has been completed or not

A to-do has a description of what needs to get done, an estimate  of the number of Pomodoros it will take to complete the task, and a status indicating if it has been completed or not.

### Record a to-do - PomoDoro
  * write the description of what needs to get done
  * estimate the number of Pomodoros to complete the todo (optional)
  * view the recorded to-do

These are the affordances the user needs to record a new assignment. Note that we haven't addressed the completion status of an assignment here. That’s because marking the to-do as complete happens outside of the to-do creation flow.

This flow seems simple, but once we begin to think about and build it out, you’ll realize there’s a lot to manage!
