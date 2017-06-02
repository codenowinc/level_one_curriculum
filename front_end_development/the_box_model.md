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


```CSS
  border: 10px solid #C0392B;
```

What are the new height and width measurements of the red `<span>`? Why?

>Give you students a moment to answer the question. Height is 110px. Width is 110px.

Now let's add a border to our blue `<span>` by adding the following code to the `.blue` class selector in the CSS.
```CSS
border: 10px solid #2980B9;
```

What are the new height and width measurements of the red `<span>`? Why?

>Give you students a moment to answer the question. Height is 110px. Width is 110px.

But it looks like we skipped padding! Let's see what happens if we give our red `<span>` a padding of 5px. Add the following code to the `.red` class selector in the CSS.
```CSS
padding: 5px;
```
