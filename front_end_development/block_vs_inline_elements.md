# Block vs. Inline Elements

Although we never use HTML to affect the layout of content on our page, all HTML elements fall into two broad display categories. Block level elements and Inline elements. Every tag in HTML is predefined as a block level element or an inline element.

## Block Level Elements
Block level elements take up the entire width of the line they're on, regardless of the amount of content within the tag. A block level element can't have anything come before or after it on the same line. they can contain other block and inline HTML elements.

Here are some HTML elements that are block level by default:
  * p
  * h1, h2, h3, h4, h5, h6
  * ol, ul
  * blockquote
  * dl
  * div
  * fieldset
  * form
  * hr
  * noscript
  * table

## Inline Elements
Inline elements are only as wide as the content within the tags. They can share the line they're on with other inline elements.

Here are some HTML elements that are inline by default:
  * b, big, i, small, tt
  * abbr, acronym, cite, code, dfn, em, kbd, strong, samp, var
  * a, bdo, br, img, map, object, q, script, span, sub, sup
  * button, input, label, select, textarea

## Demonstration
To demonstrate this concept in action let's look at what happens when we take a block level element, let's say a div, and an inline element, let's say a span and map them out to see the different ways in which they occupy space on the screen.

Let's head back over to [JSBin](http://jsbin.com/ "JSBin") to see these concepts in action.

>Give your students a moment to navigate to the site. The purpose of this follow along exercise is to demonstrate the differences in how block level and inline elements take up space on the page.

The first thing we're going to do is add our tags to the the HTML tab. Add three block-level `<div>` tags to with the content Block 1, Block 2, and Block 3. Then we'll add three inline level `<span>` tags with the content Inline 1, Inline 2, and Inline 3.

*JSBin HTML*
```HTML
<div>Block 1</div>
<div>Block 2</div>
<div>Block 3</div>
<span>Inline 1</span>
<span>Inline 2</span>
<span>Inline 3</span>
```

When looking at the output, we immediately realize that the three block-level div elements each occupy an entire line, while the three inline span elements only occupy as much space as they need to fit the content inside them.

We can better see the footprint of each element by using CSS to add a background color to each div and span element.

*JSBin CSS*
```CSS
div{
  background-color: #F1C40F;
}

span{
  background-color: #34495e;
  color: #ECF0F1;
}
```

>View the final JSBin snapshot [here](http://jsbin.com/cosozu/11/edit?html,css,output "Final JSBin Snapshot").

We can see the footprint of each element by looking at the background color of each div and span element. Note how the block-level `<div>` tags take up the entire width of the output screen while the inline `<span>` tags only take up as much space as the content inside of them.

Understanding the difference between block-level and inline elements is crucial when it comes to the layout of your content and learning how to position HTML elements on the page. We'll be using these concepts heavily as we move forward.

>If there is time, feel free to go into the different ways in which block-level elements can be positioned and resized versus inline elements. You can use JSBin to demonstrate how block-level elements can be given a fixed height and width but inline elements can not.

## The CSS `display:` Property
It is important to note that you can change the the default display level of an element by using the `display:` property in CSS and providing one of the three following values: inline, block, and **inline-block**.

>Explain the `inline-block` value to your students. Show them a demonstration in JSBin. Have them change the display property for the heading on their show page, so it appears in line with the checkbox instead of on the line underneath.

```CSS
h2{
  display: inline-block;
  vertical-align: middle;
  font-size: 32px;
  margin: 20px 0px;
}
```

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Make show.html heading inline-block"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.

