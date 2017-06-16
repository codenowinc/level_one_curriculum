# Make Your HTML Smart

Now that we have created our todo Index and Show pages in our Rails application, it's time to use some of the powers Rails gives us to make our HTML smart.

## The Objective
Our goal is to have a show page for every todo in our list, not just the first one. Ideally, we'd like to have a show page for each todo. That seems simple enough! All we need to do is write the HTML for each todo's show page, just like we have done for the first todo in our lists. So In the example todo application, we have seven todos in the list, so we'd need seven show pages. But wait, what happens when we add another todo to the list? We have to create a whole new file and write the HTML for that todo's show page? That's not very practical! Let's take a look at how to make our HTML smart so we can add as many todos to our lists as we want, and a show page is created for each one automatically. Better yet, let's do that with only one show.html.erb file!

## Embdedded Ruby
Take a look at the file name of your view files. Like we talked about earlier, you’ll notice they have the file extension .html.erb. We know that the .html extension designates that this file has HTML in it. Does anyone remember what the .erb extension stands for?

>Give your students a moment to volunteer an answer.

The .erb file extension stands for embedded Ruby. This indicates that the file can contain both HTML and Ruby code.

This is one of the most powerful abilities Rails gives you. You will be able to process logic in your HTML view files, and output the results of that logic to the screen the user sees in the browser.

Let’s see embedded Ruby in action! Before you can write Ruby code in your view file, you have to learn about embedded Ruby tags. Embedded Ruby tags are special characters that surround any Ruby code we write in the view file, so Rails knows how to differentiate between the HTML and the Ruby.

Here is what some embedded Ruby looks like in an html.erb file:
```html.erb
<h1>Example HTML Document with Ruby</h1>
<p>Let's do some math</p>
4 + 3 = <%= 4+3 %>
```
