# HTML Starts With Content

## Add Your Content
The main purpose of HTML is to manage the content we want to display on the web. So we'll start by entering our content into our HTML file. Write out the title of this page. Write out your list of actual to-dos that you and your partner have to complete within the next week. Remember you'll also need a link on this page to add a new to-do to the list. All we're going to do is type the words that reflect what we want to appear on the page.

>Give the students 2-3 minutes to complete this. Cut and paste the code below into your index.html file in Cloud9. Run the server and show the students what it looks like. Ask them if theirs looks similar.

*index.html*
```HTML
Workshop Todo List
Make the curriculum 4 pomodoros
Buy workshop supplies 3 pomodoros
Meet with the volunteer trainers 2 pomodoros
Order food for Saturday and Sunday 1 pomodoro
Check pre-work assignments 2 pomodoros
Send workshop location to all the students 1 pomodoro
Have a great workshop 0 pomodoros
Add todo
```

## What is HTML?
HTML stand for Hyper Text Markup Language. HTML consists of tags that we wrap around our content. These tags are semantic, meaning they describe the content that they are wrapping. For example, below we have a paragraph of filler text. To indicate to HTML that this content is a paragraph, we'd wrap it in `<p></p>` tags like so.
```HTML
<p>
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Doloremque officia dignissimos,
  dolorem voluptatem, laborum ut nemo facilis in sapiente corporis molestiae, iusto vero consequatur
  fuga quaerat! Numquam qui nemo, similique.
</p>
```

We wrap our content in tags so that we have a hook by which to grab or refer to specific pieces of content. Let's learn a little more about HTML tags.

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add content to index.html"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
