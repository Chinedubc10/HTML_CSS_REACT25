CSS Basics
Cascading Style Sheets (CSS) is what makes the web visually appealing by defining how HTML elements are styled and laid out. Here's a beginner-friendly overview of CSS to get you started.

What is CSS?
CSS stands for Cascading Style Sheets.
It controls the look and feel of a web page, including layout, colors, fonts, and more.
CSS separates content (HTML) from presentation (styling).
CSS Syntax and Selectors
CSS Syntax
CSS rules are written in a simple format:

selector {
property: value;
}
Selector: Targets the HTML element(s) to style.
Property: Defines the aspect to style (e.g., color, font size).
Value: Specifies the desired style.
Example:

h1 {
color: blue;
font-size: 24px;
}
Selectors
Selectors define which HTML elements are affected by CSS rules:

Type Selector: Targets elements by their tag name.

p { color: red; }
Class Selector: Targets elements with a specific class.

.highlight { background-color: yellow; }
ID Selector: Targets a single element by its ID.

#main-title { text-align: center; }
Universal Selector: Targets all elements.

- { margin: 0; }
  Including CSS in HTML
  Inline CSS (Inside an HTML element):

<p style="color: green;">This text is green.</p>
Internal CSS (Inside a <style> tag in the <head>):

<style>
  body { font-family: Arial, sans-serif; }
</style>

External CSS (In a separate .css file):

<link rel="stylesheet" href="styles.css">
Recommended for large projects as it keeps HTML clean and reusable.
Comments
CSS comments help you document your code:

/_ This is a comment in CSS _/
h1 { color: blue; } /_ Style for headings _/
Comments are ignored by the browser and are useful for leaving notes or explanations.
Basic CSS to Start
Styling HTML Elements
Headings and Paragraphs
h1 {
font-size: 32px;
color: navy;
}
p {
color: gray;
line-height: 1.5;
}
Lists
ul {
list-style-type: square;
padding-left: 20px;
}
ol {
list-style-type: decimal;
padding-left: 20px;
}
Links
a {
color: blue;
text-decoration: none;
}
a:hover {
text-decoration: underline;
color: darkblue;
}
Images
img {
max-width: 100%;
height: auto;
border: 1px solid #ccc;
}
Page Layout and Background
body {
font-family: Arial, sans-serif;
margin: 0;
padding: 0;
background-color: #f9f9f9;
}
Practical Example
This example combines semantic HTML elements with basic CSS styling:

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Semantic HTML with CSS</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
      background-color: #f9f9f9;
    }
    h1 {
      color: navy;
      font-size: 28px;
    }
    p {
      color: gray;
      line-height: 1.6;
    }
    a {
      color: blue;
      text-decoration: none;
    }
    a:hover {
      text-decoration: underline;
      color: darkblue;
    }
  </style>
</head>
<body>
  <h1>Welcome to Semantic HTML with CSS</h1>
  <p>This page demonstrates how to style semantic HTML elements using CSS.</p>
  <a href="#">Learn more</a>
</body>
</html>
