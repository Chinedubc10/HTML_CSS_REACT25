CSS Pseudo-Classes and Pseudo-Elements
Pseudo-classes and pseudo-elements are powerful tools in CSS that allow you to style elements based on their state or specific parts of their content without adding extra HTML.

Pseudo-Classes
A pseudo-class selects elements based on their state, position, or interaction. It’s written as selector:pseudo-class {}.

Common Pseudo-Classes
Hover, Focus, and Active
Used for interactive elements like buttons and links.

a:hover {
color: red; /_ Changes color when hovered _/
}

input:focus {
border-color: blue; /_ Highlights input when clicked _/
}

button:active {
background-color: darkblue; /_ Changes color when clicked _/
}
First and Last Child
Targets the first or last element within a parent.

p:first-child {
font-weight: bold;
}

p:last-child {
font-style: italic;
}
nth-Child and nth-of-Type
Allows targeting elements in a pattern.

li:nth-child(odd) {
background-color: lightgray; /_ Styles every odd list item _/
}

li:nth-child(3) {
color: blue; /_ Styles the third list item _/
}

p:nth-of-type(2) {
color: red; /_ Styles only the second paragraph inside a section _/
}
Empty, Not, and Checked
div:empty {
border: 1px solid red; /_ Styles empty divs _/
}

input:not([type="text"]) {
background: lightblue; /_ Styles all inputs except text inputs _/
}

input:checked {
outline: 2px solid green; /_ Highlights selected checkboxes or radio buttons _/
}
Pseudo-Elements
A pseudo-element selects and styles specific parts of an element’s content. It’s written as selector::pseudo-element {} (with double colons ::).

First Letter and First Line
Used for typography styling.

p::first-letter {
font-size: 2em;
font-weight: bold;
color: red;
}

p::first-line {
font-style: italic;
}
Selection Styling
Changes how text appears when highlighted by the user.

p::selection {
background: yellow;
color: black;
}
Before and After
Adds content before or after an element without modifying the HTML.

h1::before {
content: "🔥 "; /_ Adds an emoji before every h1 _/
}

h1::after {
content: " 🎉"; /_ Adds an emoji after every h1 _/
}
Practical Use Cases
Highlight required form fields:

input:required {
border: 2px solid red;
}
Create a striped table with nth-child:

tr:nth-child(even) {
background-color: #f2f2f2;
}
Style placeholder text:

input::placeholder {
color: gray;
font-style: italic;
}
Summary
Pseudo-classes apply styles based on state (:hover, :nth-child, :checked).
Pseudo-elements style parts of an element (::before, ::after, ::first-letter).
Use ::before and ::after for content injection.
:not() helps exclude elements from styles.
