# The Box Model
Every HTML element on the page can be though of as a box. Regardless of what the elements look like on the page, their footprint is that of a box. In CSS, the term "box model" is used when talking about the design and layout of your content.

There are four elements that make up the box that is every HTML element: content, padding, border and margin.
![CSS Box Model](/images/the_box_model/01.png "CSS Box Model")

## Breaking Down The Box Model
* **Content** - The content you have specified insinde the element in your HTML file
* **Padding** - An area of space directly around the content. The padding is transparent. It is used to create space between the content and the border.
* **Border**  - A visible or invisible border that goes around the content and padding of the element.
* **Margin**  - An area of space directly around the border. The margin is transparent. It is used to create space between the HTML element it wraps around and other HTML elements on the page.

Now, using the [W3 CSS Properties Resource](https://www.w3schools.com/cssref/ "W3 CSS Properties Resource"),identify the CSS properties that can be used to change the padding, border, and margin of an HTML element.

>Give your students a few minutes to find the `padding:`, `border:`, and `margin:` properties.

It is important to note that changing the padding, border, and margin of and HTML element will affect that elements height and width even if it may not look any different.

Now let's see each of these CSS properties in action.

>Use [JSBin](http://jsbin.com/ "JSBin") to demonstrate the following concepts. Open up the HTML, CSS, and Output tabs once you navigate to the service. Feel free to delete the HTML document structure tags in the HTML tab, you will not need them.


### Content
>Enter the following code into your JSBin tabs.

*JSBin HTML*
```HTML
<span class="box-one">Box 1</span>
```

*JSBin CSS*
```CSS
.box-one{
  background-color: #E74C3C;
  color: #ECF0F1;
}
```

Here we have a HTML `<span>` element with a class for which we have defined a background color and font color.

Now let's add another `<span>` element to the page and give it similar CSS style rules.

*JSBin HTML*
```HTML
<span class="box-one">Box 1</span>
<span class="box-two">Box 2</span>
```

*JSBin CSS*
```CSS
.box-one{
  background-color: #E74C3C;
  color: #ECF0F1;
}

.box-two{
  background-color: #3498DB;
  color: #ECF0F1;
}
```

Now we have two HTML `<span>` elements. The "Box 1" and "Box 2" text inside each of them is considered the content.

### Padding
Now let's see how padding affects our two `<span>` elements. In the CSS, add the following line of code to your `.box-one` and `box-two` class selectors respectively.
```CSS
padding: 5px;
```

What happens when the CSS padding property is added?

>Give you students a moment to answer the question. Space is added around the content, but the background color expands as well as it is still the element that is getting larger.

### Border
Now it's time to add a border to each `<span>` element. In the CSS, add the following line of code to your `.box-one` and `box-two` class selectors respectively.
```CSS
border: 2px solid #2C3E50;
```

We now see a thin dark line bordering each of the `<span>` elements.


### Margin
Finally it's time to add margin. In the CSS, add the following line of code to your `.box-one` and `box-two` class selectors respectively.
```CSS
margin: 5px;
```

You should see some distance created all around each of the `<span>` elements.

>View the final JSBin snapshot [here](http://jsbin.com/xetufac/54/edit?html,css,output "Final JSBin Snapshot").

## Inspect Elements
When calculating the height and width of HTML elements, remember to take into account the margin, border and padding as well. You can right-click object on a web page and choose the option to "Inspect" to see the box model that wraps it.
![CSS Box Model Inspector](/images/the_box_model/03.png "CSS Box Model Inspector")

## Apply the Concept
Let's apply what we just learned to our todo list application. Right now our todos and pomodoros estimates on our index page are scrunched together. Let's apply some padding and margin to give them a little more space.

Add the following style rule to your index.css file:
```CSS
li{
  padding: 5px;
  margin-bottom:10px;
}
```

> Give your students some time to add padding and margin to other elements on the page. The goal is for their pages to resemble the demo Todo App mockup.

## Commit and Push to GitHub
It's important to constantly commit and push your code to GitHub. This way, as you make changes and add to your code, you'll be able to save your progress and not be at risk of losing your work.

Use the following commands to commit your changes and push them to GitHub.

```shell
git add -A
```

```shell
git commit -m "Add spacing to todo in list on todo index page"
```

```shell
git push
```

Now check your repository on GitHub to see if the changes were successfully pushed.
