Box Model, Padding, Margin, and Borders
The CSS box model is a fundamental concept that defines how elements are structured and spaced in a web page. It includes the element's content, padding, border, and margin.

The CSS Box Model
Every HTML element is considered a box. The box model consists of the following components:

Content:

The inner part of the box where text and images appear.
Padding:

The space between the content and the border.
Padding increases the size of the element without affecting other elements.
Border:

The edge surrounding the padding (or content if no padding is defined).
Margin:

The space outside the border, separating the element from its neighbors.
Block and Inline Elements
Block Elements
Take up the full width of their container by default.
Respect margin, padding, and borders on all sides.
Example:

div {
display: block;
margin: 10px;
padding: 10px;
border: 2px solid black;
}
Inline Elements
Occupy only the space of their content.
Respect horizontal padding, margin, and borders (top/bottom are visible but don’t affect layout).
Example:

span {
display: inline;
margin: 5px;
padding: 5px;
border: 1px solid gray;
}
Inline-Block Elements
Behave like inline elements but respect padding, margin, and borders on all sides.
Useful for aligning items horizontally while maintaining block-like spacing.
Example:

.menu-item {
display: inline-block;
padding: 10px;
margin: 5px;
border: 1px solid black;
}
Padding
Defines the space between the content and the border.
Can be set individually for each side: padding-top, padding-right, padding-bottom, padding-left.
Shorthand
padding: 10px 20px 15px 5px; /_ Top, Right, Bottom, Left _/
Examples
div {
padding: 20px; /_ Equal padding on all sides _/
}

div {
padding: 20px 10px; /_ 20px padding on top and bottom, 10px on left and right _/
}

div {
padding: 20px 15px 10px 5px; /_ Padding: 20px on top, 15px on right, 10px on bottom, 5px on left _/
}

div {
padding-top: 30px; /_ Adds 30px of space above the content _/
padding-left: 15px; /_ Adds 15px of space to the left of the content _/
}
Border
Surrounds the padding (or content if no padding).
Properties:
border-width: Thickness of the border.
border-style: Solid, dotted, dashed, etc.
border-color: Color of the border.
Shorthand
border: 2px solid black;
Examples
div {
border: 1px solid gray; /_ Sets border width, style, and color on all sides _/
}

div {
border-width: 2px;
border-style: dashed;
border-color: blue;
}

div {
border-top: 3px dotted red; /_ 3px dotted border on top, color red _/
border-right: 2px solid green; /_ 2px solid border on right, color green _/
}
Margin
Creates space outside the border, separating elements.
Can be set individually for each side: margin-top, margin-right, margin-bottom, margin-left.
Shorthand
margin: 10px 20px 15px 5px; /_ Top, Right, Bottom, Left _/
Examples
div {
margin: 20px; /_ Equal margin on all sides _/
}

div {
margin: 20px 10px; /_ 20px margin on top and bottom, 10px on left and right _/
}

div {
margin-top: 30px;
margin-right: 15px;
}
Auto Margin for Centering
Margins can automatically center block-level elements horizontally:

div {
margin: 0 auto;
width: 50%;
}
Box Sizing
Controls how the total size of the element is calculated.
content-box: Width and height include only the content.
border-box: Width and height include padding and border.
div {
box-sizing: border-box;
}
Border Radius
Rounds the corners of an element.

Examples
div {
border: 2px solid black;
border-radius: 10px;
}

div {
border-radius: 50%;
}
Border Image
Uses an image as the border for an element.

Example
div {
border: 20px solid transparent;
border-image: url('border-image.png') 30 round;
}
Outline
A line drawn outside the border, not part of the box model.

Example
div {
outline: 2px dotted red;
}
Practical Example
CSS:

.box {
width: 200px;
height: 100px;
padding: 20px;
border: 3px solid black;
border-radius: 15px;
margin: 20px auto;
text-align: center;
}
HTML:

<div class="box">
  Box Model Example
</div>
