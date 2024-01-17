JavaScript – 
JavaScript is a lightweight, cross-platform, object-oriented scripting language used to makes web pages dynamic and interactive. It is one of the three core technologies of web development. It can be used in Client-side and Server-side. 
JavaScript was invented by Brendan Eich in 1995, It was developed for Netscape 2 and became an ECMA standard in 1997.
ECMA-262 is the official name of the standard. ECMAScript is the official name of the language.
Scripting language  - A scripting language is a programming language that employs a high-level construct to interpret and execute commands one by one at run time. It don’t need the compilation step
•	Client-side JavaScript extends the core language by supplying objects to control a browser and its Document Object Model (DOM). For example, client-side extensions allow an application to place elements on an HTML form and respond to user events such as mouse clicks, form input, and page navigation.
•	Server-side JavaScript extends the core language by supplying objects relevant to running JavaScript on a server. For example, server-side extensions allow an application to communicate with a database, provide continuity of information from one invocation to another of the application, or perform file manipulations on a server.

Notes – 
Ending statements with semicolon is not required, but highly recommended.
JavaScript keywords are reserved words. Reserved words cannot be used as names for variables.
Numbers are not allowed as the first character in names.
This way JavaScript can easily distinguish identifiers from numbers.
JavaScript is Case Sensitive
Hyphens are not allowed in JavaScript. They are reserved for subtractions.
JavaScript accepts both double and single quotes:
JavaScript is the default scripting language in HTML
A JavaScript function is a block of JavaScript code, that can be executed when "called" for.
Using document.write() after an HTML document is loaded, will delete all existing HTML:

Comments -
 //Single line
 /*  Multi
       Line*/
In a programming language, variables are used to store data values. Values can be -
•	Fixed values
•	Variable values
Fixed values are called Literals.
Variable values are called Variables.

JavaScript Variables can be declared in 4 ways:
•	Automatically
•	Using var
•	Using let
•	Using const
Note
The var keyword was used in all JavaScript code from 1995 to 2015.
The let and const keywords were added to JavaScript(ES6) in 2015.
The var keyword should only be used in code written for older browsers.

JavaScript variable names can contain letter, digit, underscore and dollar sign. Name is case-sensitive. Name cannot start with number/digit and can’t contain reserved words.

Both let and const use the block-scope and can not be re-declared, the differnce b/w let and const is let is mutable and const is immutabel and must be initialized at the time of declaration.
Before ES6 (2015), JavaScript variables had only Global Scope and Function Scope.

let and const must be declared before use.
let and const does not bind to this.
let and const are not hoisted.
Re-Declaring JavaScript Variables
If you re-declare a JavaScript variable declared with var, it will not lose its value.
var carName = "Volvo";
var carName;

You cannot re-declare a variable declared with let or const.
let carName = "Volvo";  
let carName;     // Uncaught SyntaxError: Identifier 'carName' has already been declared

If the variable is not declared  error will be –
Uncaught ReferenceError: carName1 is not defined
Constant Objects and Arrays - 
The keyword const is a little misleading.
It does not define a constant value. It defines a constant reference to a value.
Because of this you can NOT:
•	Reassign a constant value
•	Reassign a constant array
•	Reassign a constant object
But you CAN:
•	Change the elements of constant array
•	Change the properties of constant object

Arithmetic Operators
+	Addition
-	Subtraction
*	Multiplication
**	Exponentiation (ES2016)
/	Division
%	Modulus (Division Remainder)
++	Increment
--	Decrement	
The exponentiation operator (**) raises the first operand to the power of the second operand.
let x = 5;
let z = x ** 2;
x ** y produces the same result as Math.pow(x, y).

JavaScript Type Operators
typeof	Returns the type of a variable
instanceof	Returns true if an object is an instance of an object type

JavaScript Logical Operators
&&	logical and
||	logical or
!	logical not

Bit operators work on 32 bits numbers.
Operator	Description	Example	Same as	Result	Decimal
&	AND	5 & 1	0101 & 0001	0001	 1
|	OR	5 | 1	0101 | 0001	0101	 5
~	NOT	~ 5	 ~0101	1010	 10
^	XOR	5 ^ 1	0101 ^ 0001	0100	 4
<<	left shift	5 << 1	0101 << 1	1010	 10
>>	right shift	5 >> 1	0101 >> 1	0010	  2
>>>	unsigned right shift	5 >>> 1	0101 >>> 1	0010	  2
JavaScript has 8 Datatypes
1. String   (typeof – string) 
2. Number    (typeof – number) 
3. Bigint    (typeof – bigint)
4. Boolean    (typeof – boolean) 
5. Undefined    (typeof – undefined) 
6. Null      (typeof – object) 
7. Symbol (typeof- symbol)
8. Object (typeof – object)
9.  typeof NaN	// Returns "number"
The Object Datatype
The object data type can contain:
1. An object  (typeof – object)
2. An array   (typeof – object)
3. A date   (typeof – object)
In JavaScript, a variable without a value, has the value undefined. The type is also undefined.
JavaScript BigInt variables are used to store big integer values that are too big to be represented by a normal JavaScript Number.
Symbol : Symbols provide a way to create unique identifiers without the risk of name collisions, making them a valuable addition to the JavaScript language for creating more robust and predictable code.
JavaScript function -
A JavaScript function is a block of code used to perform a particular task. The code inside a function is executed when invoke(call). Function help us to re-use block of code multiple time with different arguments.
JavaScript Object –
Accessing Object Properties
objectName.propertyName  or  objectName["propertyName"]
Avoid String, Number, and Boolean objects. They complicate your code and slow down execution speed.
x = new String();        // Declares x as a String object
y = new Number();        // Declares y as a Number object
z = new Boolean();       // Declares z as a Boolean object

<!DOCTYPE html>
<html>
<body>
<h2>JavaScript</h2>
<p>When adding a number and a string, JavaScript will treat the number as a string.</p>
<p id="demo1"></p>
<p id="demo2"></p>
<p id="demo3"></p>
<p id="demo4"></p>
<p id="demo5"></p>
<p id="demo6"></p>
<p id="demo7"></p>
<p id="demo8"></p>
<p id="demo9"></p>

<script>
let a = true;
let b = "Volvo";
let c = 10;
let d = null;
let e = undefined;
const f = BigInt(12345678901234567890123441235);
const arr = ['a', 'b'];
const obj = {a: 1, b: 2};
const fun = function() {return this.firstName + " " + this.lastName;}
document.getElementById("demo1").innerHTML = typeof(a);
document.getElementById("demo2").innerHTML = typeof(b);
document.getElementById("demo3").innerHTML = typeof(c);
document.getElementById("demo4").innerHTML = typeof(d);
document.getElementById("demo5").innerHTML = typeof(e);
document.getElementById("demo6").innerHTML = typeof(f);
document.getElementById("demo7").innerHTML = typeof(arr);
document.getElementById("demo8").innerHTML = typeof(obj);
document.getElementById("demo9").innerHTML = typeof(fun);
</script>
</body>
</html>

HTML Event
Events are triggered either by browser or user interaction.
Event			Description
onchange		An HTML element has been changed
onclick		The user clicks an HTML element
onmouseover	The user moves the mouse over an HTML element
onmouseout		The user moves the mouse away from an HTML element
onkeydown		The user pushes a keyboard key
onload		The browser has finished loading the page

JavaScript Strings
JavaScript strings are for storing and manipulating text.
To find the length of a string, use the built-in length property:
The backslash (\) escape character turns special characters into string characters:
code Result	Description
\'	'	Single quote
\"	"	Double quote
\\	\	Backslash

Six other escape sequences are valid in JavaScript:
Code	Result
\b	Backspace
\f	Form Feed
\n	New Line
\r	Carriage Return
\t	Horizontal Tabulator
\v	Vertical Tabulator
The 6 escape characters above were originally designed to control typewriters, teletypes, and fax machines. They do not make any sense in HTML.
Comparing two JavaScript objects always returns false.

String Methods - 
String length
String slice()
String substring()
String substr()
String replace()
String replaceAll()
String toUpperCase()
String toLowerCase()
String concat()	String trim()
String trimStart()
String trimEnd()
String padStart()
String padEnd()
String charAt()
String charCodeAt()
String split()
Extracting String Parts
There are 3 methods for extracting a part of a string:
•	slice(start, end)
•	substring(start, end)
•	substr(start, length)
slice() extracts a part of a string and returns the extracted part in a new string.
If you omit the second parameter, the method will slice out the rest of the string:
If a parameter is negative, the position is counted from the end of the string:
substring()
The difference is that start and end values less than 0 are treated as 0 in substring().

substr()
The difference is that the second parameter specifies the length of the extracted part.
If the first parameter is negative, the position counts from the end of the string.

Replace –
The replace() method replaces a specified value with another value in a string:
The replace() method does not change the string it is called on.
The replace() method returns a new string.
The replace() method replaces only the first match
If you want to replace all matches, use a regular expression with the /g flag set.
By default, the replace() method is case sensitive.
To replace case insensitive, use a regular expression with an /i flag (insensitive):
let newText = text.replace(/MICROSOFT/i, "W3Schools");
Regular expressions are written without quotes.
To replace all matches, use a regular expression with a /g flag (global match):
let newText = text.replace(/Microsoft/g, "W3Schools");
The replaceAll() method allows you to specify a regular expression instead of a string to be replaced.
replaceAll() is an ES2021 feature.
replaceAll() does not work in Internet Explorer.
A string is converted to upper case with toUpperCase():
A string is converted to lower case with toLowerCase():
concat() joins two or more strings:
The concat() method can be used instead of the plus operator. These two lines do the same:
Note
All string methods return a new string. They don't modify the original string.
Formally said:
Strings are immutable: Strings cannot be changed, only replaced.

trim()
ECMAScript 2019 added the string methods trimStart and trimEnd() to JavaScript.
The trim() method removes whitespace from both sides of a string:
The trimStart() method works like trim(), but removes whitespace only from the start of a string.
The trimEnd() method works like trim(), but removes whitespace only from the end of a string.
let text1 = "      Hello World!      ";

ECMAScript 2017 added two new string methods to JavaScript: padStart() and padEnd() to support padding at the beginning and at the end of a string.
Pad a string with "x" until it reaches the length 4:
let text = "5";
let padded = text.padStart(4,"x");    //xxx5
Pad a string with "x" until it reaches the length 4:
let text = "5";
let padded = text.padEnd(4,"x");      ///5xxx
To pad a number, convert the number to a string first.

Extracting String Characters
There are 3 methods for extracting string characters:
•	charAt(position)
•	charCodeAt(position)
•	Property access [ ]
chatAt() : The charAt() method returns the character at a specified index (position) in a string:
charCodeAt() : The charCodeAt() method returns the unicode of the character at a specified index in a string:
text[0] = "A";    // Gives no error, but does not work

Converting a String to an Array
If you want to work with a string as an array, you can convert it to an array.
A string can be converted to an array with the split() method:
If the separator is omitted, the returned array will contain the whole string in index [0].
If the separator is "", the returned array will be an array of single characters.

String Search Methods
•	String indexOf()
•	String lastIndexOf()
•	String search()
•	String match()
•	String matchAll()
•	String includes()
•	String startsWith()
•	String endsWith()

The indexOf() method returns the index (position) the first occurrence of a string in a string.
The lastIndexOf() method returns the index of the last occurrence of a specified text in a string.
Both indexOf(), and lastIndexOf() return -1 if the text is not found.
Both methods accept a second parameter as the starting position for the search.
The lastIndexOf() methods searches backwards (from the end to the beginning), meaning: if the second parameter is 15, the search starts at position 15, and searches to the beginning of the string.

The search() method searches a string for a string (or a regular expression) and returns the position of the match
The two methods are NOT equal. These are the differences:
•	The search() method cannot take a second start position argument.
•	The indexOf() method cannot take powerful search values (regular expressions).
The match() method returns an array containing the results of matching a string against a string (or a regular expression).
let text = "The rain in SPAIN stays mainly in the plain";
text.match(/ain/gi);  // ain,AIN,ain,ain
The matchAll() method returns an iterator containing the results of matching a string against a string (or a regular expression).
If the parameter is a regular expression, the global flag (g) must be set, otherwise a TypeError is thrown.
const iterator = text.matchAll(/Cats/g);
matchAll() is an ES2020 feature.
matchAll() does not work in Internet Explorer.
JavaScript String includes()
The includes() method returns true if a string contains a specified value.
Otherwise it returns false.
let text = "Hello world, welcome to the universe.";
text.includes("world", 12);

includes() / startsWith() is case sensitive.
includes() / startsWith() is an ES6 feature.
includes() / startsWith() is not supported in Internet Explorer.

includes() method case insensitive, convert both of the strings in the comparison to lowercase.
let text = "Hello world, welcome to the universe.";
text.startsWith("world", 6)

The startsWith() method returns true if a string begins with a specified value.
Otherwise it returns false:
text.startsWith("world", 6)
The endsWith() method returns true if a string ends with a specified value.
Otherwise it returns false:
text.endsWith("world", 11);

JavaScript Template Literals
Template Literals use back-ticks (``)
Template literals allows multiline strings
Template literals provide an easy way to interpolate variables and expressions into strings.
The method is called string interpolation  ${...}
JavaScript Number Methods
All JavaScript numbers are stored as decimal numbers (floating point).
JavaScript integers are only accurate up to 15 digits:
In JavaScript, all numbers are stored in a 64-bit floating-point format (IEEE 754 standard).
Infinity (or -Infinity) is the value JavaScript will return if you calculate a number outside the largest possible number.
Division by 0 (zero) also generates Infinity.
Infinity is a number: typeof Infinity returns number.
By default, JavaScript displays numbers as base 10 decimals.
But you can use the toString() method to output numbers from base 2 to base 36.
Hexadecimal is base 16. Decimal is base 10. Octal is base 8. Binary is base 2.
Method		Description
toString()		Returns a number as a string
toExponential()	Returns a number written in exponential notation
toFixed()		Returns a number written with a number of decimals
toPrecision()	Returns a number written with a specified length
ValueOf()		Returns a number as a number

The toString() method returns a number as a string.
toExponential() returns a string, with a number rounded and written using exponential notation.
toFixed() returns a string, with the number written with a specified number of decimals:
let x = 9.656;
  x.toFixed(0) + "<br>" +    //10
  x.toFixed(2) + "<br>" +    //9.66
  x.toFixed(4) + "<br>" +    //9.6560
  x.toFixed(6);                      //9.656000
toPrecision() returns a string, with a number written with a specified length:
let x = 9.656;
x.toPrecision();    //9.656
x.toPrecision(2);   //9.6
x.toPrecision(4);   //9.656
x.toPrecision(6);   //9.65600

valueOf() returns a number as a number.
All JavaScript data types have a valueOf() and a toString() method.

Number()	Returns a number converted from its argument.
parseFloat()	Parses its argument and returns a floating point number
parseInt()	Parses its argument and returns a whole number
If the number cannot be converted, NaN (Not a Number) is returned.
ES6 also added 2 new methods to the Number object:
•	Number.isInteger()
•	Number.isSafeInteger()
JavaScript Array –
An array is a special type of object that allows you to store multiple values in a single variable.
const array_name = [item1, item2, ...];      
Converting an Array to a String
The JavaScript method toString() converts an array to a string of (comma separated) array values.
Array Properties and Methods
cars.length   // Returns the number of elements
cars.sort()   // Sorts an array alphabetically:
Associative Arrays
Arrays with named indexes are called associative arrays (or hashes).
JavaScript does not support arrays with named indexes.
WARNING !!
If you use named indexes, JavaScript will redefine the array to an object.
After that, some array methods and properties will produce incorrect results.
In JavaScript, arrays use numbered indexes, objects use named indexes.
JavaScript new Array()
These two different statements both create a new array containing 2 numbers:
const points = new Array(40, 100);
const points = [40, 100];
A Common Error
const points = [40];
is not the same as:
const points = new Array(40);     // Create an array with 40 undefined elements:
How do I know if a variable is an array?
The problem is that the JavaScript operator typeof returns "object":
Solution 1 - To solve this problem ECMAScript 5 (JavaScript 2009) defined a new method Array.isArray().  Array.isArray(fruits);
Solution 2 - The instanceof operator returns true if an object is created by a given constructor. fruits instanceof Array;
Array length
Array toString()
Array pop()
Array push()
Array shift()
Array unshift()	Array join()
Array delete()
Array concat()
Array flat()
Array splice()
Array slice()

- toString() convert array into comma separated string. arrayName.toString().
- join() method joins all array elements into a string with specified separator as an argument.
- pop()  remove the last element from an array. X = arrayName.pop() and returns the value that was “popped out”.
- shift() remove the first array element and shift all other elements to a lower index. arrayName.shift(). And return the string that was “shifted out”
- push()  add new element to an array(at the end). arrayName.push(element). It will return the new array length.
-unshift() add new element to an array(at the beginning), and unshift the older elements. It will return the new array length.
- delete – this will delete the element from the array and leave the place as undefined. delete arrayName[index]. Using delete may leave undefined holes in the array. Use pop() or shift() instead.
-concat() creates a new array by merging (concatenating) existing arrays, It does not change the existing arrays. It always returns a new array, It can take any number of array arguments and also take any other variable as arguments.
-flat() creates a new array with all sub-array elements concatenated into it recursively up to the specified depth.
Flattening an array is the process of reducing the dimensionality of an array.
The Infinity parameter ensures that all nested arrays are flattened, regardless of their depth. By default flat depth is one.
const nestedArray = [1, [2, 3], [4, 5, [6, 7]]];
const flattenedArray = nestedArray.flat(Infinity);
- splice() – this will add new items to an array and delete some items acc to the parameters pass. arrayName.splice(start, deleteCount, element1, element2,element3). It returns the deleted list of array. you can use splice() to remove elements without leaving "holes" in the array.
- slice() – it removes the element from the array and return the removed elements. arrayName().slice(startIndex), arrayName().slice(startIndex, endIndex), It creates new array and does not remove any elements from the source array.
If the end argument is omitted, like in the first examples, the slice() method slices out the rest of the array.
-reverse() method reverses the elements in an array.
JavaScript Sorting Arrays
-sort() - By default sort() function will work properly for strings only(A-Za-z). And it will produce incorrect result for numbers. So for numeric values we can use compare() function.
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a - b});
Use the same trick to sort an array descending:
points.sort(function(a, b){return b - a});
Sorting an Array in Random Order
points.sort(function(){return 0.5 - Math.random()});
Note - The java.lang.Math.random() method returns a pseudorandom double type number greater than or equal to 0.0 and less than 1.0.
MAX and Min value in array –
You can use Math.max.apply to find the highest number in an array:
Math.max.apply(null, arr);
You can use Math.min.apply to find the lowest number in an array:
Math.min.apply(null, arr);

JavaScript Array Iteration
-forEach() method calls a function (a callback function) once for each array element. It takes 3 arguments –
forEach(element, index(optional), array(optional)) => { } and always return undefined and any manipulation will work inside the body of forEach().
-map() method creates a new array by performing a function on each array element. It takes 3 arguments –
map(element, index(optional), array(optional)) => { } and returns new array, without changing the original array.
-flatMap() method in JavaScript is a combination of the map() and flat() methods. It first maps each element using a mapping function and then flattens the result into a new array. It takes 3 arguments –
flatMap(element, index(optional), array(optional)) => { } and returns new array, without changing the original array.
-filter() work on conditions of array and return those elements which satisfy the conditions. It takes 3 arguments –
- filter (element, index(optional), array(optional)) => { } and returns new array
-reduce() method runs a function on each array element to produce (reduce it to) a single value, it works from left-to-right in the array, It doesn’t modify the original array. takes 4 arguments:
•	The total (the initial value / previously returned value)
•	The item value
•	The item index
•	The array itself
-reduceRight() works from right-to-left in the array.
-every() checks, whether all elements in the array pass a provided function's test. It returns a Boolean value: true if the callback function returns a truthy value for every element in the array, and false otherwise.
[45, 4, 9, 16, 25].every((value) => value > 3);  //true
-some() checks, whether at least one element in the array passes a provided function's test. It returns a Boolean value: true if the callback function returns a truthy value for any element in the array, and false otherwise.
-indexOf() method searches an element value in an array and returns its position.
array.indexOf(item(required), start(optional))  
start: Where to start the search. Negative values will start at the given position counting from the end, and search to the end.
Array.indexOf() returns -1 if the item is not found.
If the item is present more than once, it returns the position of the first occurrence.
-lastIndexOf returns the position of the last occurrence of the specified element in an array.
array.lastIndexOf (item(required), start(optional))
start: Where to start the search. Negative values will start at the given position counting from the end, and search to the beginning
-find() method returns the value of the first array element that passes a test function. It takes 3 arguments –
find(element, index(optional), array(optional)) => { }
-findIndex() method returns the index of the first array element that passes a test function. It takes 3 arguments –
findIndex (element, index(optional), array(optional)) => { }
- Array.from() method returns an Array object from any object with a length property or any iterable object.
Array.from("ABCDEFG");
{Array.from({ length: numberOfIterations }, (_, index) => (
        <div key={index}>Count: {index + 1}</div>
      ))}
- check if an element is present in an array (including NaN, unlike indexOf)
array.includes(search-item)
-Spread –The ... operator expands an iterable
Truthy and falsy values
-	Falsy values: undefine, null, 0, ‘ ’, NaN.
-	Truthy values: Not falsy values.
-	Comparing two JavaScript objects always return false.
New Date Object()
Date objects are static. The "clock" is not "running"
By default, JavaScript will use the browser's time zone and display a date as a full text string:
Thu Dec 21 2023 15:50:55 GMT+0530 (India Standard Time)
Date objects are created with the new Date() constructor.
There are 9 ways to create a new date object:
new Date()
new Date(date string)
new Date(year,month)
new Date(year,month,day)
new Date(year,month,day,hours)
new Date(year,month,day,hours,minutes)
new Date(year,month,day,hours,minutes,seconds)
new Date(year,month,day,hours,minutes,seconds,ms) YYYY-MM-DDTHH:MM:SSZ
new Date(milliseconds)
JavaScript counts months from 0 to 11:
January = 0, December = 11.

JavaScript stores dates as number of milliseconds since January 01, 1970.
You cannot omit month. If you supply only one parameter it will be treated as milliseconds.
date objects, using either local time or UTC (universal, or GMT(Greenwich Mean Time)) time.
UTC time is the same as GMT

let date = new Date();   //Sat Feb 13 2021 18:48:44 GMT+0530 (India Standard Time)
date.toDateString();      //Sat Feb 13 2021
date.toUTCstring();      //Sat, 13 Feb 2021 13:20:10 GMT Coordinated Universal Time
date.toISOString();       //2021-02-13T13:20:35.060Z  The International Standard Org
If you have a valid date string, you can use the Date.parse() method to convert it to milliseconds.
Date.parse() returns the number of milliseconds between the date and January 1, 1970:
let msec = Date.parse("March 21, 2012");
One and two digit years will be interpreted as 19xx:

Date Get Methods
Method		Description
getFullYear()	Get year as a four digit number (yyyy)
getMonth()		Get month as a number (0-11)
getDate()		Get day as a number (1-31)
getDay()		Get weekday as a number (0-6)
getHours()		Get hour (0-23)
getMinutes()	Get minute (0-59)
getSeconds()	Get second (0-59)
getMilliseconds()	Get millisecond (0-999)
getTime()		Get time (milliseconds since January 1, 1970)
toLocaleString()	Converts a Date object to a string, using locale conventions

You can use an array of names to return the month as a name:
const months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];

const d = new Date("2021-03-25");
let month = months[d.getMonth()];

You can use an array of names, and getDay() to return weekday as a name
const days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];

const d = new Date("2021-03-25");
let day = days[d.getDay()];

UTC Date Get Methods
Method			Same As		Description
getUTCDate()		getDate()		Returns the UTC date
getUTCFullYear()		getFullYear()	Returns the UTC year
getUTCMonth()		getMonth()		Returns the UTC month
getUTCDay()			getDay()		Returns the UTC day
getUTCHours()		getHours()		Returns the UTC hour
getUTCMinutes()		getMinutes()	Returns the UTC minutes
getUTCSeconds()		getSeconds()	Returns the UTC seconds
getUTCMilliseconds()	getMilliseconds()    Returns the UTC milliseconds

The getTimezoneOffset() method returns the difference (in minutes) between local time an UTC time

Set Date Methods
Method		Description
setDate()		Set the day as a number (1-31)
setFullYear()		Set the year (optionally month and day)
setHours()		Set the hour (0-23)
setMilliseconds()	Set the milliseconds (0-999)
setMinutes()	Set the minutes (0-59)
setMonth()		Set the month (0-11)
setSeconds()	Set the seconds (0-59)
setTime()		Set the time (milliseconds since January 1, 1970)

Math Object
The JavaScript Math object allows you to perform mathematical tasks on numbers.
Unlike other objects, the Math object has no constructor.
The Math object is static.
All methods and properties can be used without creating a Math object first.
Math.round(x)	Returns x rounded to its nearest integer
Math.ceil(x)		Returns x rounded up to its nearest integer
Math.floor(x)	Returns x rounded down to its nearest integer
Math.trunc(x)	Returns the integer part of x (new in ES6)
Math.sign(x) 	Returns if x is negative(-1), null(0) or positive(1). (new in ES6)
Math.pow(x, y) 	Returns the value of x to the power of y:
Math.sqrt(x)  	Returns the square root of x:
Math.abs(x) 		Returns the absolute (positive) value of x
Math.sin(x) 		Returns the sine (a value between -1 and 1) of the angle x (given in radians).
Angle in radians = Math.sin(90 * Math.PI / 180);     // returns 1 (the sine of 90 degrees)
Math.cos(x) 	Returns the cosine (a value between -1 and 1) of the angle x (given in radians).
Angle in radians = Math.cos(0 * Math.PI / 180);     // returns 1 (the cos of 0 degrees)
Math.min() and Math.max() can be used to find the lowest or highest value in a list of arguments:
Math.random() 	Returns a random number between 0 (inclusive), and 1 (exclusive):

Nullish Coalescing Operator (??)
The ?? operator returns the first argument if it is not nullish (null or undefined).
Otherwise it returns the second argument.
Optional Chaining Operator (?.)
The ?. operator returns undefined if an object is undefined or null (instead of throwing an error).
Break - 
In JavaScript, the break keyword is used within loop structures (for, while, do-while) and switch statements to immediately exit the loop or switch block when executed.
The break statement "jumps out" of a loop.
Note: If you omit the break statement, the next case will be executed even if the evaluation does not match the case.
It is not necessary to break the last case in a switch block. The block breaks (ends) there anyway. Switch cases use strict comparison (===).
Continue -
The continue statement "jumps over" one iteration in the loop.
The continue statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.
For In Loop
The JavaScript for in statement loops through the properties of an Object:
For object -
for (key in object) {
  // code block to be executed
}
const person = {fname:"John", lname:"Doe", age:25};
let text = "";
for (let x in person) {
  text += person[x];
}
For Array –
for (variable in array) {
  code
}
const numbers = [45, 4, 9, 16, 25];
let txt = "";
for (let x in numbers) {
  txt += numbers[x];
}

Do not use for in over an Array if the index order is important.
The index order is implementation-dependent, and array values may not be accessed in the order you expect.

For Of Loop
for (let x of language) {
text += x;
}
Iterating
•	Iterating over a String
•	Iterating over an Array

JavaScript Set – 
A JavaScript Set is a collection of unique values.
Each value can only occur once in a Set.
Method		Description
new Set()		Creates a new Set
add()			Adds a new element to the Set
delete()		Removes an element from a Set
has()			Returns true if a value exists in the Set
forEach()		Invokes a callback for each element in the Set
values()		Returns an iterator with all the values in a Set
Property		Description
size			Returns the number of elements in a Set
to access values in set –
letters.values()   // Returns [object Set Iterator]
const letters = new Set(["a","b","c"]);
// List all Elements
let text = "";
for (const x of letters.values()) {
  text += x;
}
JavaScript Map -
A Map holds key-value pairs where the keys can be any datatype.
A Map remembers the original insertion order of the keys.
Method		Description
new Map()		Creates a new Map
set()			Sets the value for a key in a Map
get()			Gets the value for a key in a Map
delete()		Removes a Map element specified by the key
has()			Returns true if a key exists in a Map
forEach()		Calls a function for each key/value pair in a Map
entries()		Returns an iterator with the [key, value] pairs in a Map
Property		Description
size			Returns the number of elements in a Map
// Create a Map
const fruits = new Map([
  ["apples", 500],
  ["bananas", 300],
  ["oranges", 200]
]);
fruits.set("oranges", 200);
JavaScript Objects vs Maps
		Object					Map
Iterable	Not directly iterable			Directly iterable
Size		Do not have a size property		Have a size property
Key Types	Keys must be Strings (or Symbols)	Keys can be any datatype
Key Order	Keys are not well ordered		Keys are ordered by insertion
Defaults	Have default keys				Do not have default keys

Type Conversion – 
JavaScript variables can be converted to a new variable and another data type:
•	By the use of a JavaScript function
•	Automatically by JavaScript itself
For String conversion there are two methods – 
1.	String(arg)    //it will give the output of string type.
2.	toString()     // it will give the output of string type.
Converting Booleans to Numbers
Number(false)     // returns 0
Number(true)      // returns 1
JavaScript Regular Expressions
A regular expression is a sequence of characters that forms a search pattern.
The search pattern can be used for text search and text replace operations.
Modifier	Description	
i		Perform case-insensitive matching	
g		Perform a global match (find all)	
m		Perform multiline matching	
d		Perform start and end matching (New in ES2022)

JavaScript try and catch
The try statement allows you to define a block of code to be tested for errors while it is being executed.
The catch statement allows you to define a block of code to be executed, if an error occurs in the try block.
JavaScript Throws Errors
When an error occurs, JavaScript will normally stop and generate an error message.
The technical term for this is: JavaScript will throw an exception (throw an error).
JavaScript will actually create an Error object with two properties: name and message.
throw Statement
The throw statement allows you to create a custom error.
If you use throw together with try and catch, you can control program flow and generate custom error messages.
finally Statement
The finally statement lets you execute code, after try and catch, regardless of the result:
Example – 
try {
    if(x.trim() == "") throw "is empty";
    if(isNaN(x)) throw "is not a number";
    x = Number(x);
    if(x > 10) throw "is too high";
    if(x < 5) throw "is too low";
  }
  catch(err) {
    message.innerHTML = "Error: " + err + ".";
  }
  finally {
    document.getElementById("demo").value = "";
  }
JS Hosting –
Hoisting is JavaScript's default behavior of moving all declarations to the top of the current scope (to the top of the current script or the current function).

The let and const Keywords
Variables defined with let and const are hoisted to the top of the block, but not initialized.
Meaning: The block of code is aware of the variable, but it cannot be used until it has been declared.
Using a let variable before it is declared will result in a ReferenceError.
Using a const variable before it is declared, is a syntax error, so the code will simply not run.
The variable is in a "temporal dead zone" from the start of the block until it is declared:
Hoisting applies to variable declarations and to function declarations.
Because of this, JavaScript functions can be called before they are declared:
myFunction(5);
function myFunction(y) {
  return y * y;
}
Functions defined using an expression are not hoisted.

JavaScript Use Strict
"use strict"; Defines that JavaScript code should be executed in "strict mode".
Strict mode is declared by adding "use strict"; to the beginning of a script or a function.
Declared at the beginning of a script, it has global scope (all code in the script will execute in strict mode):
Declared inside a function, it has local scope (only the code inside the function is in strict mode):
Strict mode makes it easier to write "secure" JavaScript.
Strict mode changes previously accepted "bad syntax" into real errors.
Not Allowed in Strict Mode -
Using a variable, without declaring it, is not allowed:
Deleting a variable, function, (or object) is not allowed.
Duplicating a parameter name is not allowed:
Writing to a read-only or get-only property is not allowed.
Function Expressions
A JavaScript function can also be defined using an expression. function expression can be stored in a variable called as an anonymous function (a function without a name).
const x = function (a, b) {return a * b};
let z = x(4, 3);
IIFE(Immediately Invoked function experssions) - 
IIFE is a function in JavaScript that runs as soon as it is defined. It is also called as anonymous self-invoking function
(function(){
 console.log("wipro");
 })();
Arrow functions -
Arrow functions allows a short syntax for writing function expressions.
// ES5
var x = function(x, y) {
  return x * y;
}
// ES6
const x = (x, y) => x * y;
Arrow functions do not have their own this. They are not well suited for defining object methods.
Arrow functions are not hoisted. They must be defined before they are used.
Function Rest Parameter -
The rest parameter (...) allows a function to treat an indefinite number of arguments as an array:
function sum(...args) {
…}
let x = sum(4, 9, 16, 25, 29, 100, 66, 77);
This Keyword -
In JavaScript, the this keyword is a special identifier that is automatically defined in the scope of every function. The value of this is determined by the invocation context (how a function is called) and can change depending on the way a function is invoked. 
1. Global Context:
In the global context (outside of any function or object), this refers to the global object. In browsers, the global object is window.
2. Function Context:
In the context of a regular function, the value of this depends on how the function is called:
•	Function Invocation: In non-strict mode, this refers to the global object (window in browsers) in function invocation. In strict mode, it is undefined.
function displayThis() {
  console.log(this);
}
displayThis(); // window (in a browser)
•	Method Invocation: When a function is called as a method of an object, this refers to the object that owns the method.
const obj = {
  name: 'Object',
  displayName: function() {
    console.log(this.name);
  }
};
obj.displayName(); // Object
•	Constructor Invocation: When a function is used as a constructor (with the new keyword), this refers to the newly created instance.
function Person(name) {
  this.name = name;
}
const person = new Person('John');
console.log(person.name); // John
•	Event Handlers: In event handlers, this refers to the element that fired the event.
document.getElementById('myButton').addEventListener('click', function() {
  console.log(this.id); // myButton
});
Call, Apply, and Bind Methods: The call(), apply(), and bind() methods allow you to explicitly set the value of this when calling a function.

3. Arrow Functions:
Arrow functions do not have their own this value. Instead, they inherit the this value from the surrounding (enclosing) lexical context.
function displayThis() {
  const arrowFunc = () => {
    console.log(this);
  };
  arrowFunc();
}
displayThis(); // Logs the value of `this` from displayThis

In JavaScript all functions are object methods.
If a function is not a method of a JavaScript object, it is a function of the global object
call() –
The call() method invokes a function and allows you to pass in arguments one by one.
Syntax - 
function.call(thisArg, arg1, arg2, ...);
Ex - 
function greet(greeting) {
  console.log(`${greeting}, ${this.name}`);
}
const person = { name: 'John' };
greet.call(person, 'Hello'); // Outputs: Hello, John
apply() - 
The apply() method is similar to call(), but it takes an array-like object (or an iterable object) as its second argument, which contains the arguments to be passed to the function.
Syntax -
function.apply(thisArg, [argsArray]);\
Ex -
function greet(greeting) {
  console.log(`${greeting}, ${this.name}`);
}
const person = { name: 'John' };
greet.apply(person, ['Hello']); // Outputs: Hello, John

bind() - 
The bind() method returns a new function, where this is permanently bound to the value specified during the bind() call. It does not invoke the function directly, instead, it call the build function with required arguments.
Syntax -
function.bind(thisArg, arg1, arg2, ...);
Ex -
function greet(greeting) {
  console.log(`${greeting}, ${this.name}`);
}
const person = { name: 'John' };
const greetJohn = greet.bind(person);
greetJohn('Hello'); // Outputs: Hello, John

Bind, call and Apply method. 
var rinku = {
  name : 'Sanskar Sharma',
  age : 19,
  work : 'student',
  presentation : function(style, time){
    if(style == 'formal'){
    console.log('Good ' + time + ' I \'m ' + this.name + ' I \'m ' +this.age + ' old' + ' I \'m a ' + this.work);
    }else{
    console.log('hey ' + time + ' what\'s up ' + this.name + ' I \'m ' +this.age + ' old' + ' I \'m a ' + this.work);
    }
  }
}

rinku.presentation('formal', 'morning');

var prachi = {
  name: 'Prachi Sharma',
  age: 23,
  work: 'software engineer',
}

prachi.presentation = rinku.presentation;
prachi.presentation('friendly','aftrenon');

rinku.presentation.call(prachi, 'formal','evening');
var p = rinku.presentation.bind(prachi, 'friendly');

p('afternoon');
p('evening')
Note
Variables created without a declaration keyword (var, let, or const) are always global, even if they are created inside a function.
Closure in javaScript –
An inner function has always access to the variable and parameters of its outer function, even after the outer function has returned, finish execution.
Closure is the function with preserve data.
Lexical scoping – a function that is lexically within another function gets access to the scope of the outer function. 
function outerFunction(outerVariable) {
  return function innerFunction(innerVariable) {
    console.log(outerVariable + innerVariable);
  };
}
const closure = outerFunction(10);
closure(5);  // Outputs: 15
JavaScript Classes
JavaScript classes were introduced in ECMAScript 2015 (ES6) to provide a more structured and familiar way to define object-oriented programming concepts in JavaScript. While JavaScript is a prototype-based language, the introduction of classes brought a syntax similar to class-based languages like Java or C++.
Class Definition: A class in JavaScript is defined using the class keyword, followed by the class name. Inside the class, you can define constructor methods, instance methods, static methods, getters, setters, etc.
A JavaScript class is not an object.It is a template for JavaScript objects.
Syntax –
class ClassName {
  constructor() { ... }
}

Constructor Method
The constructor method is a special method:
•	It has to have the exact name "constructor"
•	It is executed automatically when a new object is created
•	It is used to initialize object properties
If you do not define a constructor method, JavaScript will add an empty constructor method.
<script>
class Car {
  constructor(name, year) {
    this.name = name;
    this.year = year;
  }
  age(x) {
    return x - this.year;
  }
}
const date = new Date();
let year = date.getFullYear();
const myCar = new Car("Ford", 2014);
document.getElementById("demo").innerHTML=
"My car is " + myCar.age(year) + " years old.";
</script>
Class Inheritance -
To create a class inheritance, use the extends keyword.
A class created with a class inheritance inherits all the methods from another class.
By calling the super() method in the constructor method, we call the parent's constructor method and gets access to the parent's properties and methods.
Inheritance is useful for code reusability: reuse properties and methods of an existing class when you create a new class.
JavaScript Modules –
JavaScript modules provide a way to encapsulate code and create reusable components by splitting code into multiple files, each containing a module. Modules allow for better organization, maintainability, and reusability of code in large-scale applications.
There are two types of exports: Named Exports and Default Exports.
Exporting:
Named Exports:
// math.js
export const add = (a, b) => a + b;
export const subtract = (a, b) => a - b;
Default Export:

// logger.js
export default function log(message) {
  console.log(message);
}
Importing:
Named Imports:
// main.js
import { add, subtract } from './math.js';
Default Import:
// main.js
import log from './logger.js';


JSON -
JSON (JavaScript Object Notation) is a lightweight data-interchange format.
JSON Syntax Rules
•	Data is in name/value pairs format.
•	Data is separated by commas
•	Curly braces hold objects
•	Square brackets hold arrays
The JSON format is syntactically similar to the code for creating JavaScript objects. Because of this, a JavaScript program can easily convert JSON data into JavaScript objects.
Since the format is text only, JSON data can easily be sent between computers, and used by any programming language.
JavaScript has a built in function for converting JSON strings into JavaScript objects:
JSON.parse()
JavaScript also has a built in function for converting an object into a JSON string:
JSON.stringify()
In JSON, values must be one of the following data types:
•	a string
•	a number
•	an object (JSON object)
•	an array
•	a boolean
•	null
JSON values cannot be one of the following data types:
•	a function
•	a date
•	undefined
JavaScript Best Practices
Avoid global variables, avoid new, avoid ==, avoid eval().
•	Always Declare Local Variables
•	Declarations on Top
•	Initialize Variables
•	Declare Objects and Arrays with const
•	Beware of Automatic Type Conversions, JavaScript is loosely typed.
•	Use === Comparison
•	End Your Switches with Defaults
Version –
This tutorial covers every version of JavaScript:
•	The Original JavaScript ES1 ES2 ES3 (1997-1999)
•	The First Main Revision ES5 (2009)
•	The Second Revision ES6 (2015)
•	Yearly Additions (2016, 2017, 2018, 2019, 2020)
JavaScript Callback –
In JavaScript, a callback is a function that is passed as an argument to another function and is executed after the completion of a particular operation, often an asynchronous one. Callbacks are a fundamental concept in JavaScript, especially for handling events, asynchronous operations, and higher-order functions.
JavaScript functions are executed in the sequence they are called. Not in the sequence they are defined.
Where callbacks really shine are in asynchronous functions, where one function has to wait for another function (like waiting for a file to load)
JS Callback hell -
Callback hell, also known as the pyramid of doom, refers to the situation in JavaScript where multiple nested callbacks are used, leading to code that is hard to read, maintain, and debug. This issue often arises in asynchronous programming scenarios, where operations depend on the results of previous operations, leading to deeply nested callback functions.
Synchronous: Default JS behavior -
In JavaScript, the default behavior for code execution is synchronous, meaning that statements are executed in the order they appear in the code. Synchronous code has a straightforward control flow, where each statement waits for the previous one to finish before it can execute.
JS Asynchronous –
Asynchronous javascript will not stop the current execution of code(execution thread), it will simple execute the asynchronous code in the background. enabling operations like fetching data from a server, reading files, or handling events without freezing the user interface.
Features – 
•	Allow asynchronous function to run in the background.
•	We pass in callbacks that run once the function has finished its work.
•	Move on immediately : Non-blocking!.
JavaScript Promises
In ECMAScript 2015 (ES6), promises are objects that represent the eventual completion (or failure) of an asynchronous operation, allowing you to write more readable and maintainable asynchronous code.
States: A promise can be in one of three states:
Pending: Initial state, neither fulfilled nor rejected.
Fulfilled (Resolved): The operation completed successfully.
Rejected: The operation failed or encountered an error.
<script>
const p = new Promise((res, rej) => { 
const a = 1+1+1;
if(a==2) res("succ");
else rej("fail");
});
p.then((m) => console.log(m)).catch((m) => console.log(m));
</script>


Certainly! Below is an example demonstrating how to refactor nested callbacks (callback hell) using promises in JavaScript:
<script>
getChesse = () => {
  return (new Promise((res, req) => {
    setTimeout(() => {
    	res("chesse is ready");
    }, 1000)
  })
)}
getDough = () => {
  return (new Promise((res, req) => {
    setTimeout(() => {
    	res("dough is ready");
    }, 1000)
  })
)}

getChesse()
.then((m) => {
    console.log(m);
    return getDough()
})
.then((m) => {
	console.log(m);
})
.catch((m) => { 
	console.log(m); 
});
</script>

Async Await –
async and await make promises easier to write. using async functions and the await keyword to pause the execution until a promise is resolved or rejected. It has to be noted that it only makes the async function block wait and not the whole program execution.

Example with async await –
<script>
getChesse = () => {
  return (new Promise((res, req) => {
    setTimeout(() => {
    	res("chesse is ready");
    }, 1000)
  })
)}
getDough = () => {
  return (new Promise((res, req) => {
    setTimeout(() => {
    	res("dough is ready");
    }, 1000)
  })
)}

const orderpizza = async () => {
try {
	const chess = await getChesse();
    console.log(chess);
    const dogh = await getDough();
    console.log(dogh);
    }
    catch(m) {
    console.log(m);
    };
}
orderpizza();
</script>

const getIDs = new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve([523, 883, 432, 974]);
            }, 1500);
        });

        const getRecipe = recID => {
            return new Promise((resolve, reject) => {
                setTimeout(ID => {
                    const recipe = {title: 'Fresh tomato pasta', publisher: 'Jonas'};
                    resolve(`${ID}: ${recipe.title}`);
                }, 1500, recID);
            });
        };

        const getRelated = publisher => {
            return new Promise((resolve, reject) => {
                setTimeout(pub => {
                    const recipe = {title: 'Italian Pizza', publisher: 'Jonas'};
                    resolve(`${pub}: ${recipe.title}`);
                }, 1500, publisher);
            });
        };

async function getIDis(){
  const ids = await getIDs;
  console.log(ids);
  const ids1 = await getRecipe(ids[0]);
  console.log(ids1);
  const ids2 = await getRelated('prachi');
  console.log(ids2);  
}
getIDis();

Async / Defer –
The role of async attribute is to load script file asynchronously. Script files are loaded parallel to HTML parser and once script files are loaded, HTML parser is stopped to execute script files. After script execution completion, HTML parser starts parsing the page again. 

The role of defer attribute is that it also loads script files parallel to HTML parser, but it waits for HTML parser completion before script execution. After HTML parser completion, scripts are executed and completed.

•	Async scripts are executed as soon as the script is loaded, so it doesn't guarantee the order of execution (a script you included at the end may execute before the first script file )
•	Defer scripts guarantees the order of execution in which they appear in the page.

JavaScript parsing       
JS downloading
JS executing
•	With async func – 
JavaScript parsing       
JS downloading
JS executing
•	With defer – 
JavaScript parsing       
JS downloading
JS executing

The getElementsByClassName() and getElementsByTagName() methods return a live HTMLCollection.
The querySelectorAll() method returns a static NodeList.
The childNodes property returns a live NodeList.
BOM –
The Browser Object Model (BOM) allows JavaScript to "talk to" the browser.
The window object is supported by all browsers. It represents the browser's window.
All global JavaScript objects, functions, and variables automatically become members of the window object.
Window properties and functions, properties return the sizes in pixels
•	window.innerHeight - the inner height of the browser window (in pixels)
•	window.innerWidth - the inner width of the browser window (in pixels)
•	window.open() - open a new window
•	window.close() - close the current window
•	window.moveTo() - moves the current window to the specified coordinates. moveTo(x, y)
•	.window.resizeTo() - method dynamically resizes the current window.
JS Screen -
The window.screen object contains information about the user's screen.
The window.screen object can be written without the window prefix.
Properties:
•	screen.width
•	screen.height
•	screen.availWidth
•	screen.availHeight
•	screen.colorDepth
•	screen.pixelDepth
JS Location -
The window.location object can be used to get the current page address (URL) and to redirect the browser to a new page.
The window.location object can be written without the window prefix.
 Properties -
•	window.location.href returns the href (URL) of the current page
•	window.location.hostname returns the domain name of the web host
•	window.location.pathname returns the path and filename of the current page
•	window.location.protocol returns the web protocol used (http: or https:)
•	window.location.assign() loads a new document
JS History -
The window.history object contains the browsers history.
Some methods:
•	history.back() - same as clicking back in the browser
•	history.forward() - same as clicking forward in the browser
•	 window.history.go(-2);
History Object Properties -
Property	Description
length	Returns the number of URLs in the history list
History Object Methods -
Method	Description
back()	Loads the previous URL in the history list
forward()	Loads the next URL in the history list
go()	Loads a specific URL from the history list
JS Popup Box -
JavaScript has three kind of popup boxes: Alert box, Confirm box, and Prompt box.
Alert Box –
The alert() method in JavaScript is used to display a dialog box with a specified message and an OK button. user must click the OK button to close the dialog and continue with the execution of the script.
window.alert("sometext");
Line Break - alert("Hello\nHow are you?");
Confirm Box - 
A confirm box is often used if you want the user to verify or accept something. the user will have to click either "OK" or "Cancel" to proceed.
If the user clicks "OK", the box returns true. If the user clicks "Cancel", the box returns false.
Prompt Box -
A prompt box is often used if you want the user to input a value before entering a page.
When a prompt box pops up, the user will have to click either "OK" or "Cancel" to proceed after entering an input value.
If the user clicks "OK" the box returns the input value. If the user clicks "Cancel" the box returns null.
window.prompt("sometext","defaultText");
Example –
let person = prompt("Please enter your name", "Harry Potter");
let text;
if (person == null || person == "") {
  text = "User cancelled the prompt.";
} else {
  text = "Hello " + person + "! How are you today?";
}

JS Timing –
The window object allows execution of code at specified time intervals.
These time intervals are called timing events.
The two key methods to use with JavaScript are:
•	setTimeout(function, milliseconds)
Executes a function, after waiting a specified number of milliseconds.
window.setTimeout(function, milliseconds);
•	setInterval(function, milliseconds)
Same as setTimeout(), but repeats the execution of the function continuously.
window.setInterval(function, milliseconds);
Stop the Execution -
The clearTimeout() method stops the execution of the function specified in setTimeout().
Syntax -
window.clearTimeout(timeoutVariable)
example-
myVar = setTimeout(function, milliseconds);
clearTimeout(myVar);

Cookies – 
Cookies are small pieces of data that websites store on the user's device, typically in the web browser, to remember information about the user and track their interactions with the website. Cookies are widely used in web development to implement various functionalities, such as session management, user authentication, personalization, tracking, and analytics.
Cookies were invented to solve the problem "how to remember information about the user"
JavaScript can create, read, and delete cookies with the document.cookie property.
Size: Cookies have a limited size (usually up to 4KB), which restricts the amount of data that can be stored in a single cookie.

Create –
document.cookie = "username=John Doe";
You can also add an expiry date (in UTC time). By default, the cookie is deleted when the browser is closed:
document.cookie = "username=John Doe; expires=Thu, 18 Dec 2013 12:00:00 UTC";
With a path parameter, you can tell the browser what path the cookie belongs to. By default, the cookie belongs to the current page.
document.cookie = "username=John Doe; expires=Thu, 18 Dec 2013 12:00:00 UTC; path=/";
Read –
let x = document.cookie;
document.cookie will return all cookies in one string much like: cookie1=value; cookie2=value; cookie3=value;
Delete - 
document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";
No need to specify a cookie value when deleting a cookie. Just set the expires parameter to a past date.
define the cookie path to ensure that you delete the right cookie.
Some browsers will not let you delete a cookie if you don't specify the path.
When deleting a cookie, you are removing the value associated with the cookie, not the key itself.
Spread – 
The spread operator (...) in JavaScript allows you to spread or unpack the elements of an iterable (e.g., arrays, strings, objects) into individual elements. 
Shallow Copy: When using the spread operator to copy arrays and objects, it performs a shallow copy, meaning nested arrays and objects are copied by reference, not cloned. If you need to deep copy nested arrays and objects, you can use libraries like lodash or implement custom deep copy functions.
Examples -
const combined = [...arr1, ...arr2];
const extended = [...original, 4, 5];
const combined = { ...obj1, ...obj2 };
const chars = [...str];
const result = sum(...numbers); // 6
Rest –
The rest operator (...) in JavaScript is a powerful feature that allows you to represent an indefinite number of arguments as an array within a function. By leveraging the rest operator, you can create variadic functions that accept variable-length argument lists, combine and manipulate arrays and objects, and simplify complex data transformations and operations.
function functionName(...paramName) {
  // Function body
}
Variadic Function:
function sum(...numbers) {
  return numbers.reduce((acc, num) => acc + num, 0);
}
console.log(sum(1, 2, 3, 4, 5)); // 15
Destructuring with Rest:
const [first, second, ...rest] = [1, 2, 3, 4, 5];
console.log(first); // 1
console.log(second); // 2
console.log(rest); // [3, 4, 5]
IndexedDB - 
IndexedDB is a powerful client-side storage API provided by modern web browsers, enabling web applications to store, retrieve, and manipulate structured data locally within the user's browser. By leveraging IndexedDB, developers can create robust, scalable, and responsive web applications that offer offline capabilities, enhanced performance, and improved user experiences.
The W3C has announced that the Web SQL database is a deprecated local storage specification so web developer should not use this technology any more. indexeddb is an alternative for web SQL data base and more effective than older technologies.
IndexedDB itself doesn't have a fixed storage limit, but The size limit for IndexedDB storage is determined by the web browser and the available disk space on the user's device, with browser-specific defaults and policies governing storage allocation and management.
Command lines – 
	mkdir  -- to create folder.
	copy NUL filename –to create the file.
	copy filename .. –to create the file.
	dir  -- to know the directories.
	cd  -- to go inside the folder.
	cd .. –to come out to parent folder.
	cls – for clear screen.
	copy filename .. – to copy the file into the parent folder.
	move filename .. – it will move the file to the parent folder.
	del filename – to del the file.
	rmdir /S foldername – to delete the folder.
	Start filename – to open the file.
For javascript npm project
	npm init.
	npm install webpack –save-dev
	npm jquery –save
Web API?
API stands for Application Programming Interface.
A Browser API can extend the functionality of a web browser.
A Server API can extend the functionality of a web server.
Web Worker?
When executing scripts in an HTML page, the page becomes unresponsive until the script is finished.
A web worker is a JavaScript that runs in the background, independently of other scripts, without affecting the performance of the page. You can continue to do whatever you want: clicking, selecting things, etc., while the web worker runs in the background.
<script>
let w;
function startWorker() {
  if (typeof(w) == "undefined") {
    w = new Worker("demo_workers.js");
  }
  w.onmessage = function(event) {
    document.getElementById("result").innerHTML = event.data;
  };
}
function stopWorker() {
  w.terminate();
  w = undefined;
}
</script>
Since web workers are in external files, they do not have access to the following JavaScript objects:
•	The window object
•	The document object
•	The parent object
Web Geolocation API
Locate the User's Position
The HTML Geolocation API is used to get the geographical position of a user.
Since this can compromise privacy, the position is not available unless the user approves it.
The Geolocation API will only work on secure contexts such as HTTPS.
The getCurrentPosition() method returns an object on success. The latitude, longitude and accuracy properties are always returned. The other properties are returned if available:
watchPosition() - Returns the current position of the user and continues to return updated position as the user moves (like the GPS in a car).
clearWatch() - Stops the watchPosition() method.
AJAX –
AJAX (Asynchronous JavaScript and XML) is a technique used in web development to create asynchronous web applications, enabling data to be exchanged between the web browser and the server without requiring a full page reload. AJAX allows you to make HTTP requests (e.g., GET, POST) to the server, retrieve data, and update parts of a web page dynamically, enhancing the user experience by providing faster and more interactive web applications.
Fetch Api –
The Fetch API provides a modern and promise-based interface for making HTTP requests in JavaScript, offering a more efficient, flexible, and developer-friendly alternative to the traditional XMLHttpRequest (XHR) object.
Get -
// Define the URL endpoint
const url = 'https://api.example.com/data';

// Make a GET request using the Fetch API
fetch(url)
  .then(response => {
    // Check if the response is successful (HTTP status code between 200-299)
    if (response.ok) {
      // Parse the JSON response
      return response.json();
    } else {
      // Handle errors (e.g., display error message)
      throw new Error(`HTTP error! Status: ${response.status}`);
    }
  })
  .then(data => {
    // Process the JSON data
    console.log(data);
  })
  .catch(error => {
    // Handle errors (e.g., display error message)
    console.error('Fetch error:', error.message);
  });

Post –
// Define the URL endpoint
const url = 'https://api.example.com/data';
// Define the data payload
const data = {
  id: 1,
  name: 'John Doe',
  email: 'john.doe@example.com'
};
// Make a POST request using the Fetch API
fetch(url, {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify(data)
})
  .then(response => {
    // Check if the response is successful (HTTP status code between 200-299)
    if (response.ok) {
      // Parse the JSON response
      return response.json();
    } else {
      // Handle errors (e.g., display error message)
      throw new Error(`HTTP error! Status: ${response.status}`);
    }
  })
  .then(data => {
    // Process the JSON data
    console.log(data);
  })
  .catch(error => {
    // Handle errors (e.g., display error message)
    console.error('Fetch error:', error.message);
  });

