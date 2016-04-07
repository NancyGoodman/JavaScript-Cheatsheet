
EXAMPLES ON index1.html and app.js

// this is a single line comment

/* this is a multiline
comment */




WHAT IS JAVASCRIPT?

	- A client side scripting language
	- Meant to run entirely on the user's browser
	- Deﬁned by the ECMAscript standard, published by the ECMA foundation
	- JavaScript != Java, they're completely different languages

DOM = Document Object Model represents all of the elements on the web page (interface to the website: html, css, etc.)

WHAT IS JAVASCRIPT USED FOR?

	- Javascript allows you to interact with the DOM to do things like:
	- Showing and hiding elements
	- Animating elements
	- Replacing elements with other elements
	- Making requests to the server without reloading the page


EXAMPLE OF JS FUNCTIONALITY:

EX: ADD NUMBERS IN BUTTONS (click to add): Function gets called on click
DEFINE FUNCTION, ASSIGN VALUES. parseInt means data type is integers and not text.
This is also an example of Logging Directly to HTML (you change the innerHTML when you click)

on .js file 

<script>
  function addNums() {
    num1 = document.getElementById("num1").value;
    num2 = document.getElementById("num2").value;
    document.getElementById("result").innerHTML = (parseInt(num1) + parseInt(num2));
  }
</script>

Necessary HTML (on html file)

  Number 1: <input type="text" id="num1">
  Number 2: <input type="text" id="num2">
  <button id="add" onclick="addNums()">Click to add</button>
  <br>
  Result: <span id="result"></span>


- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 


VARIABLES

Value Types
Number 		numeric value (parse text to be numeric)
String 		characters inside quotes
Boolean 	true or false
Null 		no value
Object 		value associated with object



Number
	var num1 = 5;
	var num2 = 17;

String 
	("cat" "dog" "fish")

Boolean
	uses if, else if, else
	for true or false return

Null


- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 


FUNCTION
Does something. Takes an action value computated/returned
EXAMPLE addNums (add numbers and return value)

<!-- Necessary HTML -->	
Number 1: <input type="text" id="num1">
Number 2: <input type="text" id="num2">
<button id="add" onclick="addNums()">Click to add</button>
<br>
Result: <span id="result"></span>

<script>
function addNums() {
  num1 = document.getElementById("num1").value;
  num2 = document.getElementById("num2").value;
  document.getElementById("result").innerHTML = (parseInt(num1) + parseInt(num2));
}
</script>


- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 


DEBUGGING (alerts, console, writing to HTML element)

- - - - - - - - - - - - 

ALERTS: 
a function that returns a popup window
do them in the console or in the .js file

<script>
alert("hello!");
</script>


<script>
function catNames(name) {
  return alert("a good cat name is " + name);
}
catNames("Daisy");
catNames("Ziggy");
</script>


HTML return alert on click
<button onclick="myFunction()">Click Me</button>
<script>
function myFunction() {
alert("I am an alert box!");
}
</script>

- - - - - - - - - - - - 

CONSOLE
Run Javascript directly on console or 
see output of javascript written in editor -->
Type this alert on the console:

alert("hello!");

Type math on the console:

2+2


Show results:
console.log(result);
or 
console.log(num1 + num2);
etc.

- - - - - - - - - - - - 

LOGGING (WRITING) DIRECTLY TO HTML
Line 1: Declare a function called change 
Line 2: Inside of the function, retrieve the current HTML document. 
	Inside of that document, retrieve the element with the ID 'el' using the getElementById function. 
	Set the content inside of the element to say "New Text".   
Line 3: Close the function. 
Line 4: In your HTML document, you'll need a <div> with the ID "el". 
	The onclick attribute allows you to specify a function to run when the element is clicked, in this case "change()" 

<script>
  function change(){ 
  document.getElementById('el').innerHTML = "NEW TEXT"; 
}
</script>

In HTML
<div onclick="change()" id="el">CHANGE ME</div>


- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 


BASIC DATA TYPES

String - "Hello World"
Number - 5, 5.5, 1000 (all numbers in JS are ﬂoats)
Boolean - true, false
Undefined - no value (when you ask for something that doesn't exist)

- - - - - - - - - - - - 

VARIABLES
a variable is a container for a value

var name = "Zach";
var numberOfWidgets = 10; 
var isCodingCool = true;

- - - - - - - - - - - - 

BASIC MATH
JavaScript can do all basic math. You could run this code in the developer console:
10 + 10; 
> 20 (this is the return on the console)

var x = 100; 
x * 40; 
> 4000 (this is the return on the console)

- - - - - - - - - - - - 

ARRAYS
Arrays are used to hold a collection of data, of any data type.
Arrays are surrounded by square brackets

String:
["Snoopy", "Charlie Brown", "Patty", "Violet"];

Multiple Data Types:
[11, 15, 25, 48, 79, "elephant"];

Arrays can also be stored in variables:
var class_names = ["Julie", "Sophie", "Rob", "John"];


Accessing Array Items - INDEXES

The index of an item inside of an array corresponds to its position
from the beginning of the array
The ﬁrst item always has an index of 0 
In this array, "charlie brown" has the index of 0 and "snoopy" has the
index of 1:
["charlie brown", "snoopy"];


ARRAYCEPTION
An array can store other arrays:
// declare the first array var toyotas = ["Camry", "Prius"]; 
// declare the second array var porsches = ["Camero", "Boxer"]; 
// declare a third array that contains the first 
// and second array var cars = [toyotas, porsches];
This is called a multi-dimensional array

- - - - - - - - - - - - 

OBJECTS
Kind of like arrays, but you deﬁne the keys
Uses curly brackets
// Create an object with strings for keys 
var car = {make: 'Toyota', model: 'Prius'};
// Pull out data with bracket notation 
console.log(car['make']);
> "Toyota"
// Pull out data with dot notation 
console.log(car.model);
> "Toyota"


- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 
LOGIC


OPERATORS
=	var assignment

given that x = 5:

Operator    Description							Comparing		Returns
==			equal to							x == 8			false
												x == 5			true
												x == "5"		true

===			equal value and equal type			x === 5			true
												x === "5"		false

!=			not equal to						x != 8			true

!==			not equal value or not equal type	x !== 5			false
												x !== "5"		true
												x !== 8			true

>			greater than						x > 8			false

<			less than							x < 8			true

>=			greater than or equal to			x >= 8			false

<=			less than or equal to				x <= 8			true




TESTING
Any test returns a boolean true or false 
To test if two strings are equal:
"stringone" === "string two"; 
>false
Using three equals signs instead of two also checks the object type 
If you don't check object type, these are both true:
(10-5) == 5; 
(10-5) == "5";
If you don't use === it can cause bugs down the road!

- - - - - - - - - - - - 

The If statement
The if statement allows us to run code only if a certain test
evaluates to true
if(5>10){ 
  console.log("You'll never see this in the console because 5 is not greater than 10"); 
}
if(5<10){ 
  console.log("But you'll definitely see this"); }

- - - - - - - - - - - - 

The else Statement

The else statement runs only if the if statement is false
if(5>10){ 
  console.log("You'll never see this because 5 is not greater than 10"); 
} else{
  Console.log("You will see this though, since 5 < 10 is false"); }

- - - - - - - - - - - - 

The else if Statement
If you want to run another test before getting to else, you'll
want to use else if

if(5>10){ 
  console.log("You'll never see this because 5 is not greater than 10");
}else if(5===5){
   console.log("Yes, 5 really is equal to 5, so this will show up in the console") }
else{ 
   console.log("We won't get here because our else if evaluates to true"); 
}

- - - - - - - - - - - - 

FUNCTIONS

A function is a way to encapsulate code for later use 
It can take arguments, which are used as variables inside the
function
It usually returns a value, which can be used later on or
displayed immediately

Declare a function called addNumbers that takes two arguments: 
numberOne and otherNumber 
return the sum of numberOne, 10, and otherNumber   
call your new function, giving it 2 argument values 
numberOne = 4, otherNumber = 14 
log the result to the console 
Calling a function is also known as "invoking" it 

Example:
function addNumbers(numberOne, otherNumber){ 
return numberOne + 10 + otherNumber; 
} 
console.log(addNumbers(4, 14)); 


Example:
function alertName(somePersonsName){
return alert(somePersonsName);
}
alertName("Zach");


<!-- Declare a function that takes a name as an argument and tells the user what name they've entered, invoke it after it has been declared -->

function hiThere(name) {
return alert("hi there " + name);
}
hiThere("Ziggy");
hiThere("Sunny");


<!-- Declare a function that takes no arguments but prints something to
the console, invoke it after it has been declared -->

function saySomething() {
return console.log("this is something");
}

saySomething();
saySomething();
saySomething();



<!-- Declare a function that, depending upon which virtual "door" was
entered, tells the user they've received a different "prize" in an alert. Try running it after it has been declared a few times with each door option -->

function openDoor(doorNumber){


if(doorNumber===1){
	return alert ("you've won a new car!");
}else if(doorNumber===2){
	return alert ("you've won a blender!");
}else if (doorNumber===3){
	return alert ("you've won a million dollars!");
}else {
	return alert ("you lost! try again");
}

}
openDoor(2);
openDoor(3);
openDoor(1);

<!-- this one will return the else statement -->
openDoor(5); 









