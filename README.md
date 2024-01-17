HTML -
HTML stands for Hyper Text Markup Language for creating Web pages.
•	The <!DOCTYPE html> declaration defines that this document is an HTML5 document, declaration is not case sensitive.
•	The <html> element is the root element of an HTML page
•	The <head> element contains meta information about the HTML page
•	The <title> element specifies a title for the HTML page (which is shown in the browser's title bar or in the page's tab)
•	The <body> element defines the document's body,
The HTML <head> element is a container for the following elements: <title>, <style>, <meta>, <link>, <script>, and <base>.
History - 
Tim Berners-Lee invented www in 1989 and html in 1991, 
W3C Recommendation: HTML5 2014
The World Wide Web Consortium is the main international standards organization for the World Wide Web. Founded in 1994 and led by Tim Berners-Lee,
Consortium(a group of companies that work closely together for a particular purpose)
Tip: You can use either .htm or .html as file extension. There is no difference; it is up to you.
HTML elements -
HTML elements with no content are called empty elements.
The <br> tag defines a line break, and is an empty element without a closing tag:
HTML tags are not case sensitive: but W3C recommends lowercase in HTML
HTML Attributes provide additional information about elements
The value of the title attribute will be displayed as a tooltip when you mouse over the element:
HTML headings are title and subtitle are defined with the <h1> to <h6> tags.
HTML Horizontal Rules
The <hr> element is used to separate content in an HTML page, it is an empty tag.
The HTML <pre> element defines preformatted text.
HTML Formatting - 
<b>	Defines bold text
<em>	Defines emphasized text 
<i>	Defines a part of text in an alternate voice or mood
<small>	Defines smaller text
<strong>	Defines important text
<sub>	Defines subscripted text
<sup>	Defines superscripted text
<ins>	Defines inserted text
<del>	Defines deleted text
<mark>	Defines marked/highlighted text
HTML Quotation
BDO stands for Bi-Directional Override.
<bdo dir="rtl">This text will be written from right to left</bdo>
<abbr>	Defines an abbreviation or acronym
<address>	Defines contact information for the author/owner of a document
<bdo>	Defines the text direction
<blockquote>	Defines a section that is quoted from another source
<cite>	Defines the title of a work
<q>	Defines a short inline quotation

HTML Comment format -
Command <!-- Write your comments here -->
HTML Color Code -
An RGB color value represents RED, GREEN, and BLUE light sources.
An RGBA color value is an extension of RGB with an Alpha channel (opacity).
HEX color value #rrggbb
HTML Links-
The target attribute can have one of the following values:
•	_self - Default. Opens the document in the same window/tab as it was clicked
•	_blank - Opens the document in a new window or tab
•	_parent - Opens the document in the parent frame
•	_top - Opens the document in the full body of the window
HTML anchor tag is also used to create bookmarks, so that readers can jump to specific parts of a web page.
EX –
<h2 id="C4">Chapter 4</h2>
<a href="#C4">Jump to Chapter 4</a>
You can also add a link to a bookmark on another page:
<a href="html_demo.html#C4">Jump to Chapter 4</a>
Use mailto: scheme inside the href attribute to create a link that opens the user's email program.
<a href="mailto:someone@example.com">Send email</a>
Button as a Link
<button onclick="document.location='default.asp'">HTML Tutorial</button>
Image extension –
Abbreviation	File Format	File Extension
APNG	Animated Portable Network Graphics	.apng
GIF	Graphics Interchange Format	.gif
ICO	Microsoft Icon	.ico, .cur
JPEG	Joint Photographic Expert Group image	.jpg, .jpeg, .jfif, .pjpeg, .pjp
PNG	Portable Network Graphics	.png
SVG	Scalable Vector Graphics	.svg
HTML Image Tags
Tag	Description
<img>	Defines an image
<map>	Defines an image map
<area>	Defines a clickable area inside an image map
<picture>	Defines a container for multiple image resources
HTML Image map
HTML image maps allow you to create clickable areas on an image.
<img src="workplace.jpg" alt="Workplace" usemap="#workmap">

<map name="workmap">
  <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm">
  <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.htm">
  <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.htm">
</map>
Shape
You must define the shape of the clickable area, and you can choose one of these values:
•	rect - defines a rectangular region
•	circle - defines a circular region
•	poly - defines a polygonal region
•	default - defines the entire region
You must also define some coordinates to be able to place the clickable area onto the image. 
Background image –
Make sure the entire element is always covered, set the background-attachment property to fixed:
This way, the background image will cover the entire element, with no stretching (the image will keep its original proportions).
HTML Picture
The HTML <picture> element allows you to display different pictures for different devices or screen sizes.
The <picture> element contains one or more <source> elements, each referring to different images through the srcset attribute. This way the browser can choose the image that best fits the current view and/or device.
<picture>
  <source media="(min-width: 650px)" srcset="img_food.jpg">
  <source media="(min-width: 465px)" srcset="img_car.jpg">
  <img src="img_girl.jpg">
</picture>
Note: Always specify an <img> element as the last child element of the <picture> element. The <img> element is used by browsers that do not support the <picture> element, or if none of the <source> tags match.
The browser will use the first <source> element with matching attribute values, and ignore any following <source> elements.
Favicon – 
A favicon is a small image displayed next to the page title in the browser tab. it should be a simple image with high contrast.
<head>
  <title>My Page Title</title>
  <link rel="icon" type="image/x-icon" href="/images/favicon.ico">
</head>
HTML Lists –
<ul>	Defines an unordered list
<ol>	Defines an ordered list
<li>	Defines a list item
<dl>	Defines a description list
<dt>	Defines a term in a description list
<dd>	Describes the term in a description list
Choose List Item Marker for <ul>
The CSS list-style-type property is used to define the style of the list item marker. It can have one of the following values:
Value	Description
disc	Sets the list item marker to a bullet (default)
circle	Sets the list item marker to a circle
square	Sets the list item marker to a square
none	The list items will not be marked
Type Attribute
The type attribute of the <ol> tag, defines the type of the list item marker:

Type	Description
type="1"	The list items will be numbered with numbers (default)
type="A"	The list items will be numbered with uppercase letters
type="a"	The list items will be numbered with lowercase letters
type="I"	The list items will be numbered with uppercase roman numbers
type="i"	The list items will be numbered with lowercase roman numbers

Block-level Elements -
A block-level element always starts on a new line, and the browsers automatically add some space (a margin) before and after the element.
It takes up the full width available
Two commonly used block elements are: <p> and <div>, 
<h1>-<h6>, ul, ol, li.
Inline Elements
An inline element does not start on a new line.
An inline element only takes up as much width as necessary.
<a>, <span> and <img>
Note: An inline element cannot contain a block-level element!
Note: You cannot have more than one element with the same id in an HTML document. The id name is case sensitive! The id name must contain at least one character, cannot start with a number, and must not contain whitespaces (spaces, tabs, etc.).
HTML iframe -
An HTML iframe is used to display a web page within a web page.
<iframe src="url" title="description"></iframe>
Tip: It is a good practice to always include a title attribute for the <iframe>. This is used by screen readers to read out what the content of the iframe is.
Semantic element -
A semantic element clearly describes its meaning to both the browser and the developer.
Examples of non-semantic elements: <div> and <span> - Tells nothing about its content.
Examples of semantic elements: <form>, <table>, and <article> - Clearly defines its content.
HTML has several semantic elements that define the different parts of a web page:
•	<header> - Defines a header for a document or a section
•	<nav> - Defines a set of navigation links
•	<section> - Defines a section in a document
•	<article> - Defines an independent, self-contained content
•	<aside> - Defines content aside from the content (like a sidebar)
•	<footer> - Defines a footer for a document or a section
•	<details> - Defines additional details that the user can open and close on demand
•	<summary> - Defines a heading for the <details> element
<meta name="viewport" content="width=device-width, initial-scale=1.0">
•	The <kbd> element defines keyboard input
•	The <samp> element defines sample output from a computer program
•	The <code> element defines a piece of computer code
•	The <var> element defines a variable in programming or in a mathematical expression
•	The <pre> element defines preformatted text
Some Useful HTML Character Entities
Result	Description	Name	Number
non-breaking space	&nbsp;	&#160;	
<	less than	&lt;	&#60;
>	greater than	&gt;	&#62;
&	ampersand	&amp;	&#38;
"	double quotation mark	&quot;	&#34;
'	single quotation mark	&apos;	&#39;
¢	cent	&cent;	&#162;
£	pound	&pound;	&#163;
¥	yen	&yen;	&#165;
€	euro	&euro;	&#8364;
©	copyright	&copy;	&#169;
®	trademark	&reg;	&#174;
The Unicode Character Sets -
Unicode can be implemented by different character sets. The most commonly used encodings are UTF-8 and UTF-16:
UTF(Unicode Transformation Format)
Charset	Description
UTF-8	A variable-length character encoding (1 to 4 bytes long). UTF-8 is backwards compatible with ASCII and the preferred encoding for e-mail and web pages.
UTF-16	A variable-length character encoding. UTF-16 is used in all major operating systems like Windows, IOS, and Unix.
The first 128 characters of UTF-8 have the same binary values as ASCII, making ASCII text valid UTF-8.
Note: A URL is another word for a web address. Uniform Resource Locators.
XHTML –
XHTML stands for EXtensible HyperText Markup Language. It is a stricter, more XML-based version of HTML.


HTML form-
An HTML form is used to collect user input. The user input is most often sent to a server for processing.
The action attribute defines the action to be performed when the form is submitted.
The method attribute specifies the HTTP method to be used when submitting the form data.
The form-data can be sent as URL variables (with method="get") or as HTTP post transaction (with method="post").
The autocomplete attribute specifies whether a form should have autocomplete on or off.
When autocomplete is on, the browser automatically complete values based on values that the user has entered before.
Novalidate Specifies that the form should not be validated when submitted
Example – 
<form action="/action_page.php" target="_blank" method="get" autocomplete="on" novalidate>
The for attribute of the <label> tag should be equal to the id attribute of the <input> element to bind them together.
The input readonly attribute specifies that an input field is read-only.
The input disabled attribute specifies that an input field should be disabled.
The input size attribute specifies the visible width, in characters, of an input field.
The input maxlength attribute specifies the maximum number of characters allowed in an input field.
The input min and max attributes specify the minimum and maximum values for an input field.
The input multiple attribute specifies that the user is allowed to enter more than one value in an input field.
The input pattern attribute specifies a regular expression that the input field's value is checked against, when the form is submitted.
The input placeholder attribute specifies a short hint that describes the expected value of an input field (a sample value or a short description of the expected format).
The input required attribute specifies that an input field must be filled out before submitting the form.
The input autofocus attribute specifies that an input field should automatically get focus when the page loads.
Canvas - 
The HTML <canvas> element is used to draw graphics on a web page. via JavaScript.
The <canvas> element is only a container for graphics. You must use JavaScript to actually draw the graphics.
SVG defines scalable vector-based graphics in XML format.
Multimedia -Multimedia comes in many different formats. It can be almost anything you can hear or see, like images, music, sound, videos, records, films, animations, and more.
Note: Only MP4, WebM, and Ogg video are supported by the HTML standard.
Note: Only MP3, WAV, and Ogg audio are supported by the HTML standard.
<video width="320" height="240" autoplay muted>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
Your browser does not support the video tag.
</video>
<audio controls autoplay muted>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
Your browser does not support the audio element.
</audio>
The controls attribute adds video controls, like play, pause, and volume.
HTML YouTube Videos
The easiest way to play videos in HTML, is to use YouTube.
<iframe width="420" height="315"
src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=1&mute=1&controls=0&playlist=tgbNymZ7vqY&loop=1">
</iframe>
A comma separated list of videos to play (in addition to the original URL).
Loop - Add loop=1 to let your video loop forever.
Value 0 (default): The video will play only once.
Value 1: The video will loop (forever).
Controls - Add controls=0 to not display controls in the video player.
Value 0: Player controls does not display.
Value 1 (default): Player controls display.
Geolocation –
The HTML Geolocation API is used to get the geographical position of a user.
The getCurrentPosition(showPosition, showError) method is used to return the user's position
•	The showPosition() function outputs the Latitude and Longitude
•	showError() function outputs the error.
•	watchPosition() - Returns the current position of the user and continues to return updated position as the user moves (like the GPS in a car).
•	clearWatch() - Stops the watchPosition() method.
HTML Drag and Drop API
In HTML, any element can be dragged and dropped.
Drag and drop is a very common feature. It is when you "grab" an object and drag it to a different location.


Steps – 
•	To make an element draggable, set the draggable attribute to true
<img draggable="true">
•	ondragstart attribute calls a function, drag(event), that specifies what data to be dragged.
The dataTransfer.setData() method sets the data type and the value of the dragged data
•	The ondragover event specifies where the dragged data can be dropped. By default, data/elements cannot be dropped in other elements. To allow a drop, we must prevent the default handling of the element.
<!DOCTYPE HTML>
<html>
<head>
<style>
#div1, #div2 { float: left; width: 100px; height: 35px; margin: 10px; padding: 10px; border: 1px solid black;}
</style>
<script>
function allowDrop(ev) {
  ev.preventDefault();
}

function drag(ev) {
  ev.dataTransfer.setData("text", ev.target.id);
}

function drop(ev) {
  ev.preventDefault();
  var data = ev.dataTransfer.getData("text");
  ev.target.appendChild(document.getElementById(data));
}
</script>
</head>
<body>
<h2>Drag and Drop</h2>
<p>Drag the image back and forth between the two div elements.</p>
<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)">
  <img src="img_w3slogo.gif" draggable="true" ondragstart="drag(event)" id="drag1" width="88" height="31">
</div>
<div id="div2" ondrop="drop(event)" ondragover="allowDrop(event)"></div>
</body>
</html>
Web storage object
HTML web storage; better than cookies.
Before HTML5, application data had to be stored in cookies, included in every server request. Web storage is more secure, and large amounts of data can be stored locally, without affecting website performance.
HTML web storage provides two objects for storing data on the client:
window.localStorage - stores data with no expiration date. The data will not be deleted when the browser is closed, and will be available the next day, week, or year.
// Store
localStorage.setItem("lastname", "Smith");
document.getElementById("result").innerHTML = localStorage.getItem("lastname");
localStorage.removeItem("lastname");
window.sessionStorage - stores data for one session (data is lost when the browser tab is closed), The data is deleted when the user closes the specific browser tab.






















CSS –
CSS stands for Cascading Style Sheets for styling web pages created with HTML.
A CSS rule consists of a selector and a declaration block.
We can divide CSS selectors into five categories:
•	Simple selectors (select elements based on name, id, class)
•	Combinator selectors (select elements based on a specific relationship between them)
•	Pseudo-class selectors (select elements based on a certain state)
•	Pseudo-elements selectors (select and style a part of an element)
•	Attribute selectors (select elements based on an attribute or attribute value)
Note: An id and class name cannot start with a number!
#para1 {
  text-align: center; 
}
.center {
  text-align: center; 
}
h1, h2, p {
  text-align: center; 
}
The universal selector (*) selects all HTML elements on the page.
There are four different combinators in CSS:
•	descendant selector (space) - The descendant selector matches all elements that are descendants of a specified element.
div p {
  background-color: yellow;
}
•	child selector (>) - The child selector selects all elements that are the children of a specified element(not descendants).
div > p {
  background-color: yellow;
}
•	adjacent sibling selector (+) - The adjacent sibling selector is used to select an element that is directly after another specific element.
div + p {
  background-color: yellow;
}
•	general sibling selector (~) - The general sibling selector selects all elements that are next siblings of a specified element.
div ~ p {
  background-color: yellow;
}
Pseudo-classes -
A pseudo-class is used to define a special state of an element.
selector:pseudo-class {
  property: value;
}
:first-child	p:first-child	Selects every <p> elements that is the first child of its parent
:last-child	p:last-child	Selects every <p> elements that is the last child of its parent
:only-child	p:only-child	Selects every <p> element that is the only child of its parent
::after	p::after	Insert content after every <p> element
::before	p::before	Insert content before every <p> element
:active	a:active	Selects the active link
:checked	input:checked	Selects every checked <input> element
:disabled	input:disabled	Selects every disabled <input> element
:not(selector)	:not(p)	Selects every element that is not a <p> element
:nth-child(n)	p:nth-child(2)	Selects every <p> element that is the second child of its parent
:nth-last-child(n)	p:nth-last-child(2)	Selects every <p> element that is the second child of its parent, counting from the last child
Note: a:hover MUST come after a:link and a:visited in the CSS definition in order to be effective! a:active MUST come after a:hover in the CSS definition in order to be effective! Pseudo-class names are not case-sensitive.
Pseudo Elements
selector::pseudo-element {
  property: value;
}
Selector	Example	Example description
::after	p::after	Insert something after the content of each <p> element
::before	p::before	Insert something before the content of each <p> element
::first-letter	p::first-letter	Selects the first letter of each <p> element
::first-line	p::first-line	Selects the first line of each <p> element
::marker	::marker	Selects the markers of list items
::selection	p::selection	Selects the portion of an element that is selected by a user
Attribute selector –
Selector	Example	Example description
[attribute]	[target]	Selects all elements with a target attribute
[attribute=value]	[target="_blank"]	Selects all elements with target="_blank"
[attribute~=value]	[title~="flower"]	Selects all elements with a title attribute that contains a space-separated list of words, one of which is "flower"
[attribute|=value]	[lang|="en"]	Selects all elements with a lang attribute value starting with "en"
[attribute^=value]	a[href^="https"]	Selects all <a> elements with a href attribute value starting with "https"
[attribute$=value]	a[href$=".pdf"]	Selects all <a> elements with a href attribute value ending with ".pdf"
[attribute*=value]	a[href*="w3schools"]	Selects all <a> elements with a href attribute value containing the substring "w3schools"
/* This is a single-line comment */
/* This is
a multi-line
comment */
CSS Backgrounds
•	background-color
•	background-image: url("paper.gif");
•	background-repeat: repeat-x/ repeat-y/ no-repeat;
•	background-attachment: fixed/scroll;
•	background-position: right top
•	background (shorthand property)

Margin - 
The CSS margin properties are used to create space around elements, outside of any defined borders.
margin: top right bottom left;
margin: 25px 50px 75px;
•	top margin is 25px
•	right and left margins are 50px
•	bottom margin is 75px
margin: 25px 50px;
•	top and bottom margins are 25px
•	right and left margins are 50px
CSS height and width Values -
The height and width properties may have the following values:
•	auto - This is default. The browser calculates the height and width
•	length - Defines the height/width in px, cm, etc.
•	% - Defines the height/width in percent of the containing block
•	initial - Sets the height/width to its default value
•	inherit - The height/width will be inherited from its parent value
CSS Outline Properties -
Property	Description
outline	A shorthand property for setting outline-width, outline-style, and outline-color in one declaration
outline-color	Sets the color of an outline
outline-offset	Specifies the space between an outline and the edge or border of an element
outline-style	Sets the style of an outline
outline-width	Sets the width of an outline

CSS Text – 
CSS Alignment -
Property	Description
direction	Specifies the text direction/writing direction
text-align	Specifies the horizontal alignment of text
text-align-last	Specifies how to align the last line of a text
unicode-bidi	Used together with the direction property to set or return whether the text should be overridden to support multiple languages in the same document
vertical-align	Sets the vertical alignment of an element
CSS Decoration -
Property	Description
text-decoration	Sets all the text-decoration properties in one declaration
text-decoration-color	Specifies the color of the text-decoration
text-decoration-line	Specifies the kind of text decoration to be used (underline, overline, etc.)
text-decoration-style	Specifies the style of the text decoration (solid, dotted, etc.)
text-decoration-thickness	Specifies the thickness of the text decoration line
CSS text-transform
text-transform: uppercase;
text-transform: lowercase;
text-transform: capitalize;
CSS Spacing –
Property	Description
letter-spacing	Specifies the space between characters in a text
line-height	Specifies the line height
text-indent	Specifies the indentation of the first line in a text-block
white-space	Specifies how to handle white-space inside an element
word-spacing	Specifies the space between words in a text
CSS List -
list-style	Sets all the properties for a list in one declaration
list-style-image	Specifies an image as the list-item marker
list-style-position	Specifies the position of the list-item markers (bullet points)
list-style-type	Specifies the type of list-item marker circle/square/ upper-roman;
Display - Every HTML element has a default display value, depending on what type of element it is. The default display value for most elements is block or inline.
Position - The position property specifies the type of positioning method used for an element (static, relative, fixed, absolute or sticky). HTML elements are positioned static by default.
z-index - The z-index property specifies the stack order of an element.
CSS Overflow
The overflow property specifies whether to clip the content or to add scrollbars when the content of an element is too big to fit in the specified area.
The overflow property has the following values:
•	visible - Default. The overflow is not clipped. The content renders outside the element's box
•	hidden - The overflow is clipped, and the rest of the content will be invisible
•	scroll - The overflow is clipped, and a scrollbar is added to see the rest of the content
•	auto - Similar to scroll, but it adds scrollbars only when necessary
Property	Description
overflow	Specifies what happens if content overflows an element's box
overflow-wrap	Specifies whether or not the browser can break lines with long words, if they overflow its container
overflow-x	Specifies what to do with the left/right edges of the content if it overflows the element's content area
overflow-y	Specifies what to do with the top/bottom edges of the content if it overflows the element's content area
Note: The overflow property only works for block elements with a specified height.
Clearfix Hack -
Note: If an element is taller than the element containing it, and it is floated, it will overflow outside of its container. You can use the "clearfix hack" to fix this (see example below).
.clearfix {
  overflow: auto;
}
.clearfix::after {
  content: "";
  clear: both;
  display: table;
}
Center align anything –
With position absolute-
.center p {
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
With display flex - 
.center {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 200px;
  border: 3px solid green;
}
Note that we have set the box-sizing property to border-box. This makes sure that the padding and eventually borders are included in the total width and height of the elements.
Opacity: The opacity property specifies the opacity/transparency of an element. Its value from 0.0 - 1.0
Specificity Hierarchy
1.	Inline styles - Example: <h1 style="color: pink;">
2.	IDs - Example: #navbar
3.	Classes, pseudo-classes, attribute selectors - Example: .test, :hover, [href]
4.	Elements and pseudo-elements - Example: h1, ::before
Math Functions -
Function		Description
calc()	Allows you to perform calculations to determine CSS property values
max()	Uses the largest value, from a comma-separated list of values, as the property value
min()	Uses the smallest value, from a comma-separated list of values, as the property value
width: calc(100% - 100px);
width: max(50%, 300px);
width: min(50%, 300px);
CSS Rounded Corners
Property	Description
border-radius	A shorthand property for setting all the four border-*-*-radius properties
border-top-left-radius	Defines the shape of the border of the top-left corner
border-top-right-radius	Defines the shape of the border of the top-right corner
border-bottom-right-radius	Defines the shape of the border of the bottom-right corner
border-bottom-left-radius	Defines the shape of the border of the bottom-left corner
border-radius: 15px 50px 30px 5px;	top-left top-right bottom-right bottom-left
border-radius: 15px 50px 30px;	top-left top-right/bottom-left bottom-right
border-radius: 15px 50px;	top-left/bottom-right top-right/bottom-left
CSS Border Image Properties
Property	Description
border-image	A shorthand property for setting all the border-image-* properties
border-image-source	Specifies the path to the image to be used as a border
border-image-slice	Specifies how to slice the border image
border-image-width	Specifies the widths of the border image
border-image-outset	Specifies the amount by which the border image area extends beyond the border box
border-image-repeat	Specifies whether the border image should be repeated, rounded or stretched
Color Keywords –
Transparent - The transparent keyword is used to make a color transparent. This is often used to make a transparent background color for an element.
Currentcolor - The currentcolor keyword is like a variable that holds the current value of the color property of an element.
Inherit - The inherit keyword specifies that a property should inherit its value from its parent element.
Gradient –
CSS gradients let you display smooth transitions between two or more specified colors.
CSS defines three types of gradients:
•	Linear Gradients (goes down/up/left/right/diagonally)
background-image: linear-gradient(direction/angle, color-stop1, color-stop2, ...);
direction - to right, to bottom right
angle - 180deg
By default, direction is top to bottom.
•	Radial Gradients (defined by their center)
background-image: radial-gradient(shape size at position, start-color, ..., last-color);
By default, shape is ellipse, size is farthest-corner, and position is center.
shape - circle
•	Conic Gradients (rotated around a center point)
background-image: conic-gradient([from angle] [at position,] color [degree], color [degree], ...);
By default, angle is 0deg and position is center.
CSS Shadow Effect - 
Add shadow to text and to elements.
•	text-shadow
•	box-shadow
CSS Text Effect -
Property	Description
text-justify	Specifies how justified text should be aligned and spaced
text-overflow	Specifies how overflowed content that is not displayed should be signaled to the user
word-break	Specifies line breaking rules for non-CJK scripts
word-wrap	Allows long words to be able to be broken and wrap onto the next line
writing-mode	Specifies whether lines of text are laid out horizontally or vertically
2D transform –
transform	Applies a 2D or 3D transformation to an element
transform-origin	Allows you to change the position on transformed elements
matrix(n,n,n,n,n,n)	Defines a 2D transformation, using a matrix of six values
translate(x,y)	Defines a 2D translation, moving the element along the X- and the Y-axis
translateX(n)	Defines a 2D translation, moving the element along the X-axis
translateY(n)	Defines a 2D translation, moving the element along the Y-axis
scale(x,y)	Defines a 2D scale transformation, changing the elements width and height
scaleX(n)	Defines a 2D scale transformation, changing the element's width
scaleY(n)	Defines a 2D scale transformation, changing the element's height
rotate(angle)	Defines a 2D rotation, the angle is specified in the parameter
skew(x-angle,y-angle)	Defines a 2D skew transformation along the X- and the Y-axis
skewX(angle)	Defines a 2D skew transformation along the X-axis
skewY(angle)	Defines a 2D skew transformation along the Y-axis
3d transformation –
rotateX(angle)	Defines a 3D rotation along the X-axis
rotateY(angle)	Defines a 3D rotation along the Y-axis
rotateZ(angle)	Defines a 3D rotation along the Z-axis
CSS transitions -
CSS transitions allows you to change property values smoothly, over a given duration.
To create a transition effect, you must specify two things:
•	the CSS property you want to add an effect to
•	the duration of the effect
Note: If the duration part is not specified, the transition will have no effect, because the default value is 0.
Property	Description
transition	A shorthand property for setting the four transition properties into a single property
transition-delay	Specifies a delay (in seconds) for the transition effect
transition-duration	Specifies how many seconds or milliseconds a transition effect takes to complete
transition-property	Specifies the name of the CSS property the transition effect is for
transition-timing-function	Specifies the speed curve of the transition effect

Specify the Speed Curve of the Transition -
The transition-timing-function property specifies the speed curve of the transition effect.
ease - specifies a transition effect with a slow start, then fast, then end slowly (this is default)
linear - specifies a transition effect with the same speed from start to end
ease-in - specifies a transition effect with a slow start
ease-out - specifies a transition effect with a slow end
ease-in-out - specifies a transition effect with a slow start and end
cubic-bezier(n,n,n,n) - lets you define your own values in a cubic-bezier function

CSS Transition + Transformation
div {
  width: 100px;
  height: 100px;
  background: red;
  transition: width 2s, height 2s, transform 2s;
}

div:hover {
  width: 300px;
  height: 300px;
  transform: rotate(180deg);
} 
CSS Animations -
CSS allows animation of HTML elements without using JavaScript!
CSS Animations?
An animation lets an element gradually change from one style to another.
Keyframes hold what styles the element will have at certain times.
CSS Animation Properties
The following table lists the @keyframes rule and all the CSS animation properties:
Property	Description
@keyframes	Specifies the animation code
animation	A shorthand property for setting all the animation properties
animation-delay	Specifies a delay for the start of an animation
animation-direction	Specifies whether an animation should be played forwards, backwards or in alternate cycles
animation-duration	Specifies how long time an animation should take to complete one cycle
animation-fill-mode	Specifies a style for the element when the animation is not playing (before it starts, after it ends, or both)
animation-iteration-count	Specifies the number of times an animation should be played
animation-name	Specifies the name of the @keyframes animation
animation-play-state	Specifies whether the animation is running or paused
animation-timing-function	Specifies the speed curve of the animation
Note: The animation-duration property defines how long an animation should take to complete. If the animation-duration property is not specified, no animation will occur, because the default value is 0s (0 seconds). 
CSS Image Reflections
The box-reflect property is used to create an image reflection.
The value of the box-reflect property can be: below, above, left , or right.

CSS masking -
CSS masking allow to create a mask layer to place over an element to partially or fully hide portions of the element.
the mask-image property specifies the image to be used as a mask layer for an element.
The mask-repeat property specifies if or how a mask image will be repeated. The no-repeat value indicates that the mask image will not be repeated (the mask image will only be shown once).
Mask-image can we used with gradient and SVG.
Property	Description
mask-image	Specifies an image to be used as a mask layer for an element
mask-mode	Specifies whether the mask layer image is treated as a luminance mask or as an alpha mask
mask-origin	Specifies the origin position (the mask position area) of a mask layer image
mask-position	Sets the starting position of a mask layer image (relative to the mask position area)
mask-repeat	Specifies how the mask layer image is repeated
mask-size	Specifies the size of a mask layer image












SASS –
SASS (Syntactically Awesome Stylesheet) is a CSS pre-processor, which helps to reduce repetition with CSS and saves time. It is more stable and powerful CSS extension language that describes the style of document structurally. 
Stylesheets are getting larger, more complex, and harder to maintain. This is where a CSS pre-processor can help.
It is a super set of CSS based on JavaScript, which means it contains all the features of CSS and is an open source pre-processor, coded in Ruby.
Sass was designed by Hampton Catlin and developed by Natalie Weizenbaum in 2006. Later, Weizenbaum and Chris Eppstein used its initial version to extend the Sass with SassScript.
How Does Sass Work?
A browser does not understand Sass code. Therefore, you will need a Sass pre-processor to convert Sass code into standard CSS.
This process is called transpiling. So, you need to give a transpiler (some kind of program) some Sass code and then get some CSS code back.
Tip: Transpiling is a term for taking a source code written in one language and transform/translate it into another language.

Sass files has the ".scss" file extension.
Sass Comments -
Sass supports standard CSS comments /* comment */, and in addition it supports inline comments // comment:
Sass supports two different syntaxes.
The SCSS syntax uses the file extension .scss.
index.scss 
$myFontSize: 18px;
$myWidth: 680px;
body {
  font-size: $myFontSize; 
}
#container {
  width: $myWidth;
}
Indented syntax -
The indented syntax was Sass’s original syntax, and so it uses the file extension .sass. Because of this extension, it’s sometimes just called "Sass". The indented syntax supports all the same features as SCSS, but it uses indentation instead of curly braces and semicolons to describe the format of the document.
index.sass 
$myFontSize: 18px
$myWidth: 680px
body 
  font-size: $myFontSize
#container 
  width: $myWidth

Sass Variables –
Sass provide a feature to declare variable with $ symbol, followed by a name that can be used later.
Sass support below variables – 
•	strings
•	numbers
•	colors
•	booleans
•	lists
•	nulls
Sass Variable Scope -
Sass variables are only available at the level of nesting where they are defined(Block scope).
Using Sass !global -
The default behavior for variable scope can be overridden by using the !global switch.!global indicates that a variable is global, which means that it is accessible on all levels.
Tip: Global variables should be defined outside any rules. It could be wise to define all global variables in its own file, named "_globals.scss", and include the file with the @include keyword.
Sass Nested Rules -
Sass allow nesting CSS selectors in a way that follows the same visual hierarchy of HTML
Sass Importing Files -
Just like CSS, Sass also supports the @import directive.
The @import directive allows you to include the content of one file in another.
The CSS @import directive has a major drawback due to performance issues; it creates an extra HTTP request each time you call it. However, the Sass @import directive includes the file in the CSS; so no extra HTTP call is required at runtime!
Tip: You do not need to specify a file extension, Sass automatically assumes that you mean a .sass or .scss file. You can also import CSS files. The @import directive imports the file and any variables or mixins defined in the imported file can then be used in the main file.
// style.scss
@import 'foundation';
@use –
The @use rule is intended to replace the old @import rule, but it’s intentionally designed to work differently. @use only makes variables, functions, and mixins available within the scope of the current file. It never adds them to the global scope. This makes it easy to figure out where each name your Sass file references comes from
// style.scss
@use 'foundation/code';
@forward –
The @forward rule in Sass is used to forward all or specific members (variables, mixins, functions) from one module to another. This allows you to create a public API for your Sass modules, making certain members accessible from outside the module while still keeping others private.
// main-variables.scss
@forward 'variables' with (
  $primary-color,
  flex-center
);
Sass Partials
By default, Sass transpiles all the .scss files directly. However, when you want to import a file, you do not need the file to be transpiled directly.
Sass has a mechanism for this: If you start the filename with an underscore, Sass will not transpile it. Files named this way are called partials in Sass.
So, a partial Sass file is named with a leading underscore:
partial Sass file named "_colors.scss". (This file will not be transpiled directly to "colors.css"):
Now, if you import the partial file, omit the underscore. Sass understands that it should import the file "_colors.scss":
SASS Mixin – 
SASS Mixins with the help of @mixin directive, allow to define styles that can be re-used throughout the stylesheet
@include directive allow to use (include) the mixin.
Syntax – 
@mixin name {
  property: value;
  property: value;...
}
Example –
@mixin important-text {
  color: red;
  font-size: 25px;
  …}
Tip: A tip on hyphens and underscore in Sass: Hyphens and underscores are considered to be the same. This means that @mixin important-text { } and @mixin important_text { } are considered as the same mixin!
Syntax -
selector {
  @include mixin-name;
}
Example -
.danger {
  @include important-text;
  background-color: green;
}

Passing Variables to a Mixin -
/* Define mixin with two arguments */
@mixin bordered($color, $width) {
  border: $width solid $color;
}

.myArticle {
  @include bordered(blue, 1px);  // Call mixin with two values
}
Default Values for a Mixin -
Syntax – 
@mixin bordered($color: blue, $width: 1px) {
  border: $width solid $color;
}
.myTips {
  @include bordered($color: orange);
}
@extend: Allows a selector to inherit the styles of another selector.


