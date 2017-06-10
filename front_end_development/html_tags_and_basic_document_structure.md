# HTML Tags and Basic Document Structure

## Introduction to HTML Tags
An HTML element usually consists of a beginning tag and end tag, with the content inserted in between. HTML tags usually consist of a less than symbol, followed by the tag name, followed by a greater than symbol.

![Example of an HTML tag](/images/html_tags_and_basic_document_structure/01.png "Example of an HTML tag")

HTML tags follow a methodology called semantic tagging. This means that the tags used to wrap the content describe the kind of content that is being wrapped.

There are many predefined HTML tags. You should always strive to use the HTML tags that best describe the content they're wrapping.

Sometimes, there is no good predefined HTML tag for the type of content you have. In these cases, you can use one of HTML's more generic tags to mark the content.

HTML should be used strictly for tagging the content on your web page, and never for styling how the content looks in the browser. We use CSS for that!

## Set Up Basic Document Structure
When starting a new HTML document, there are a set of HTML tags we need to start off with by default. These tags make up the basic HTML document structure.

>Share the HTML document structure tags below with your students and have them cut and paste the tags into their index.html documents above their content.

```HTML
<html>
  <head>
    <title></title>
  </head>
  <body>

  </body>
</html>
```

Now that we have the tags that make up the basic structure of an HTML document, let's take a minute to understand what each one is for.

#### `<html></html>`
An opening <html> tag should appear first and a closing </html> tag should appear at the bottom of every HTML document. Every other bit of HTML should appear between those two tags.

#### `<head></head>`
The head is placed before the body and includes information about the web page and instructions for web browsers and search engine web crawlers. We'll talk more about what goes into the head tag as we continue to build our application.

#### `<title></title>`
Every HTML document head should contain a page title. The page title is used as the name of the web page when it appears on a search engine results page (SERP). The title is also used as a label for the browser window or tab where the web page is loaded.

Let's try updating the content between our title tags. Enter a short description that reflects the purpose of this page.

>Give your students a few seconds to update the content within the title tags and refresh their output to see how the content in the browser tab changes. The title of the sample todo application is `<title>Todo List Application</title>`

#### `<body></body>`
The `<body></body>` element contains the entire content of a webpage. It must be the second element inside of the parent `<html></html>` element, following only the `<head></head>` element.

Now that we've gotten a brief introduction to what each of these tags is for, let's move all of our content into our `<body></body>` tag.

>Give your students a minute to move their content into the body tags. Their code should look similar to the index.html file below.

*index.html*
```HTML
<html>
  <head>
    <title>Todo List Application</title>
  </head>
  <body>
    Workshop Todo List
    Make the curriculum 4 pomodoros
    Buy workshop supplies 3 pomodoros
    Meet with the volunteer trainers 2 pomodoros
    Order food for Saturday and Sunday 1 pomodoro
    Check pre-work assignments 2 pomodoros
    Send workshop location to all the students 1 pomodoro
    Have a great workshop 0 pomodoros
  </body>
</html>
```

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add HTML document structure tags"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
