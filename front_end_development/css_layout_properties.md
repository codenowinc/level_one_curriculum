# CSS Layout Properties

## Page Layout
Every web page has three components.
  1. Content
  2. Styling
  3. Layout

We've already talked about adding content to our HTML files and styling that content using CSS. Now we're going to understand the basics of using CSS to change layout.

### Display
Display is CSS's most important property for controlling layout. Every element has a default display value depending on what type of element it is. We just covered display properties in detail.

### Position
Position is another important CSS display property. It allows you to set an element's position within the viewport (which is a fancy way of describing your browser window).

The value of the position property specifies the type of positioning method used for an element. (static, relative, absolute or fixed).

The four main values of the position property:
  * static (default)
  * relative
  * fixed
  * absolute
Every HTML element has a static position by default.

#### Static
Static positioned elements are not affected by the top, bottom, left, and right properties. An element with position: static; is not positioned in any special way; it is always positioned according to the normal flow of the page.

#### Relative
An element with position: relative; is positioned relative to its normal position. Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.

#### Fixed
An element with position: fixed; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The top, right, bottom, and left properties are used to position the element. A fixed element does not leave a gap in the page where it would normally have been located. Notice the fixed element in the lower-right corner of the page.

#### Absolute
An element with position: absolute; is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed). However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.

#### Overlapping Elements
When elements are positioned, they can overlap other elements. The z-index property specifies the stack order of an element (which element should be placed in front of, or behind, the others).
