# All About Style
CSS stands for Cascading Style Sheets. It is a style sheets language that is used to describe the presentation of an HTML document. What this means is if HTML is strictly used to describe the content on your web page, CSS is used strictly to describe how that content looks and is positioned on the web  page.

CSS can be applied to HTML in a few different ways. We'll be writing our CSS in the separate CSS files your created on day one of the workshop.

## Introduction to CSS Rules
You write CSS by defining a series of what are called rules. Here is an example of a CSS rule that makes `<h1>` HTML elements orange.
![Example of a CSS rule](/images/all_about_style/01.png "Example of a CSS rule")

Each CSS rule has two major components: a selector that links the CSS rule to a specific part of the HTML document, and a set of one or more declarations.

Each declaration contains a property and a value. The property refers to the characteristic of the selector you want to change and the value refers to how you want to change the property. You can find an extensive list of CSS properties at [W3 Schools CSS Selector Reference](https://www.w3schools.com/cssref/css_selectors.asp "W3 Schools CSS Selector Reference").
![Selector, Property, Value, Declaration](/images/all_about_style/02.png "Selector, Property, Value, Declaration")

## Write Your First CSS Rule
Open the file, index.css and write the following style:
```CSS
html{
  font-family: sans-serif;
}
```
This CSS rule should change the text on your page from its default serif font, to a sans-serif font. Start your server and refresh your index page, did the style of all of your text change?

>Give your students a moment to type the style rule, and check to see if the styles were applied.

## Link Files using `<link>`
The styles of the heading was not changed, and this is because, currently, there is nothing linking the index.html file to the index.css file. The index.html does not know to apply the CSS rules in index.css. We must link the index.css stylesheet to the index.html file.

We do this by using the `<link>` HTML tag. All link tags go within the `<head>` tags at the top of your HTML document.

In Cloud9 if you type link and then hit the tab key, it will automatically complete the tag. This is shortcut you can use for any HTML tag or CSS style rule.
```HTML
<head>
  <title>Todo List Application</title>
  <link rel="stylesheet" href="">
</head>
```

The HTML `<link>` tag is another example of a self closing tag. We can see that it has an attribute called `href` just like an `<a>` tag. In the quotes, enter the name of the CSS stylesheet you want to link to this HTML file.

>Give your students a moment to link their index.css style sheet to their index.html file. They should have a `<link>` tag that looks like the code below.

```HTML
<link rel="stylesheet" href="index.css">
```

If you've linked your stylesheet to your HTML document properly, you should see the font of your heading change when you refresh your live web page.

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add first style rule and link index.css to index.html"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
