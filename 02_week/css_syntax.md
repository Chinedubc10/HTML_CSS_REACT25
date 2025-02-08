CSS Syntax, Selectors, Specificity, Inheritance, and Cascade
CSS Syntax
CSS rules follow this basic structure:

selector {
property: value;
}
Selector: Specifies the HTML element(s) to style.
Property: Defines the style attribute (e.g., color, font-size).
Value: Specifies the desired style for the property.
Example:

p {
color: blue;
font-size: 16px;
}
Selectors
CSS selectors are used to target HTML elements. Here are the most common types:

Universal Selector (\*):\*\*
Targets all elements.

- {
  margin: 0;
  padding: 0;
  }
  Type Selector:\*\*
  Targets elements by their tag name.

h1 {
color: red;
}
Class Selector (.):\*\*
Targets elements with a specific class.

.card {
background-color: lightgray;
}
ID Selector (#):\*\*
Targets a single element with a specific ID.

#header {
text-align: center;
}
Combinators\*\*
Define relationships between elements:

Descendant Combinator ( ):
Targets elements inside another element.

div p {
color: gray;
}
Child Combinator (>):
Targets direct children of an element.

ul > li {
list-style: square;
}
Adjacent Sibling Combinator (+):
Targets the next sibling of an element.

h1 + p {
font-size: 14px;
}
General Sibling Combinator (~):
Targets all siblings of an element.

h1 ~ p {
color: blue;
}
Specificity
Specificity determines which CSS rule is applied when multiple rules target the same element. Higher specificity overrides lower specificity.

Specificity Weight:
Inline styles: 1000
ID selectors: 100
Classes, attributes, pseudo-classes: 10
Type selectors and pseudo-elements: 1
/_ Specificity: 1 _/
p {
color: black;
}

/_ Specificity: 10 _/
.text {
color: blue;
}

/_ Specificity: 100 _/
#highlight {
color: green;
}

/_ Inline style: 1000 _/

<p style="color: red;">Red text</p>
Inheritance
Some CSS properties, like color and font-family, are inherited by child elements, while others (e.g., margin and padding) are not.

Forcing inheritance:
Use inherit to explicitly inherit a property:

p {
color: inherit;
}
Example:

<div style="color: red;">
  <p>This paragraph inherits red color.</p>
</div>
Cascade
The cascade determines how CSS rules are applied when there are conflicts:

Importance: Rules with !important override all others.
Specificity: More specific selectors take precedence.
Source Order: Later rules overwrite earlier ones.
/_ Lowest priority _/
p {
color: black;
}

/_ Higher specificity _/
.text {
color: blue;
}

/_ Inline style: Highest specificity _/

<p style="color: red;">This is red text</p>

/_ !important: Overrides everything _/
p {
color: green !important;
}
Practical Example
Combine what you’ve learned to style a simple layout:

HTML:

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Fundamentals</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header id="main-header" class="header">
    <h1>Welcome to CSS Basics</h1>
  </header>
  <nav class="nav">
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Contact</a>
  </nav>
  <main class="content">
    <p>This is the main content area.</p>
  </main>
</body>
</html>
CSS:

/_ Universal Selector _/

- {
  margin: 0;
  padding: 0;
  }

/_ ID Selector _/
#main-header {
background-color: lightblue;
padding: 20px;
}

/_ Class Selector _/
.nav {
text-align: center;
}

.nav a {
margin: 0 10px;
color: blue;
text-decoration: none;
}

/_ Type Selector _/
p {
font-size: 16px;
line-height: 1.5;
}
