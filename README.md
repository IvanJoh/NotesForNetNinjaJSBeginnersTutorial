# Notes for the NetNinja Tutorial on JavaScript for Beginners
In this file, I have all the notes for the tutorial that I have made while watching the videos

[playlist](https://www.youtube.com/playlist?list=PL4cUxeGkcC9i9Ae2D9Ee1RvylH38dKuET)

## Video 2
- JavaScript is one of the three core languages for web development (HTML, CSS, JS)
- JS is a scripting language and NOT a programming language
- JS is a client side language
- JS should enhance the user experience
- JavaScruipt has NOTHING to do with JAVA

## Video 5
- HTML loads from top to bottom so beware where you put the script tag for JS
- Asynchronous scripts can be put in the head tag

## Video 7
- JS is case sensitive 
- JS statements are ended with a ";"
- Not sensitive to whitespace
- JS runs from top to bottom

## Video 8
- Use variables to store information
- Define variable with "let"
- Declaring a variable allocates a space of memory to that variable
- Change the value AND type of a variable anywhere in your program
- JS has dynamic types and is weakly/loosely typed
- Variable names cannot start with a number

## Video 9
- 5 common operators are =, +, -, /, *
- "=" is the assignment operator
- "+" is addition
- "-" is subtraction
- "/" is division
- "*" is multiplication
- adding a number to a string results in a concatenation
- returns NaN when trying to do other mathematical operations on non-number data types

## Video 10
- += is shorthand to adding something to the original value
- -= is shorthand to subtracting something to the original value
- same with /= and *=
- shorthand for incrementing and decrementing are ++ and --

## Video 11
- When writing messages to the document, use document.write()
- When writing messages to the console, use console.log()

## Video 12
**Booleaans**
- A boolean is a value that represents true or false
- Use Boolean() to test the truthy or falsy values

## Video 13
**If statements and control flow**
- expressions in an if statement need to result in true for the relevant code to execute
- else statement executes if none of the if statements above it evaluated to true

## Video 14
**else if statements**
- If you want to check for multiple conditions, use else if() {}

## Video 15
**Comparison Operators**
- When using triple equals "===", that checks that the value and the type is the same

## Video 16
**Logical Operators**
- logical operators are used for multiple comparisons operations in the same expression
- && means that both comparisons need to evaluate to true for the expression to evaluate to true
- || means that either of the comparisons need to evaluate to true for the expression to evaluate to true

## Video 17
**While loops**
- A while loop is another control flow system
- A while loop iterates until the condition does not evaluate to true
```
let age = 5;

while (age < 10) {
    console.log("Your age is less than 10");
    age++;
}

document.write("you are now over 10");
```

## Video 18
**For loops**
- A for loop is anothe control flow system
- A for loop iterates for a set number of times using an index variable, a condition, and an increment/decrement
```
for (age=5; age<10; age++) {
    console.log("Your age is less than 10");
}

document.write("you are now over 10");

//Another example
let links = documenht.getElementsByTagName("a");

for(i=1; i<=links.length; i++) {
    console.log("this is link number " + i);
}
document.write("all links now looped");
```

## Video 19
**Break and Continue**
- Break keyword breaks out of the loop for good
- Continue keyword stops the current loop iteration and continues on the next loop iteration
```
for (i=0; i<10; i++) {
    if (i===5 || i===3) {
        continue;
    }
    console.log(i);
    if (i===7) {
        break;
    }
}

console.log("I have broken out of the loop");

//expected output
0
1
2
4
6
7
"I have broken out of the loop"
```

## Video 20
**Loops practical example**
See the example in ../Examples/video20/test.js

## Video 21
**Functions**
- A function is a way to group logical sections of code together
- Specify functions with the keyword function
- Call functions by their function names
- Functions can return values with the keyword return
```
function getAverage(a, b) {
    let average = (a + b)/2;
    console.log(average);
    return average;
}

let myResult = getAverage(7, 8);
console.log("the averaege is " + myResult);
```

## Video 22
**Variable Scope**
- Determines where variables are visible/can be used
- Two types of scope: local and global
- Global variables are defined outside of any functions and can therefore be called anywhere
- Local variables are defined inside a function and can only be called inside the functions they are defined in
```
function getAverage(a, b) {
    let average = (a + b)/2;//local variable
    console.log(average);
    return average;
}

let myResult = getAverage(7, 8);//global variable
console.log("the averaege is " + myResult);

function logResult() {
    console.log("the average is " + myResult + " inside the function"); //This will work, global variables inside functions
}

console.log(average)//this won't work, local variable outside scope
```

## Video 23
**Numbers**
- It is important that when you define numbers you don't put quotes around them
- The Math object has many functions attached to it that you can use when working with numbers

## Video 24
**NaN (Not a Number)**
- When you try to use math operators other than "+" (which concatenates) with non-number data types, it returns NaN
- Use built-in JS function isNaN() to check input that is required to be of data type number
```
let a = "apple";
let b = 5;

if (!isNaN(a)) {//notice the negation
    console.log("meaning of life is " + (a + b));
} else {
    console.log("that aint even a number, thickie");
}
```

## Video 25
**Strings**
- Take note of the quotation marks that you don't accidentally close off your string
- Escape characters in a string with back slash '\'
- All strings have access to certain methods including: indexOf(), length, toUpperCase()
```
let myString = 'I\'m a "fun" string';

let string1 = "abc";
let string2 = "ABC";

console.log(string1.toLowerCase() === string2.toLowerCase());//returns true
```

## Video 26
**Slice and Split Strings**
- Use slice to get a section of a string: string.slice(2, -2);
- Use split to divide a string into sections and put into an array: string.split(", ");

## Video 27
**Arrays**
- An array is a single variable that can hold multiple values
- Use square brackets for an array: []
- Arrays also have methods that you can use to metadata for arrays
```
let myArray = [];

myArray[0] = 25;

myArray[1] = 35;

//explicitly define the array
let myArray2 = [25, 35]; 

//You can use the array prototype to create arrays
let myArray3 = new Array();
```

## Video 28
**Introduction to Objects**
- JS uses a simplified version of objects
- All data types are objects with methods that you can use
- Object data types are also objects with methods and have the object structure {}
- Methods are called with (), properties are called without(e.g. string.length)

## Video 29
**Creating a new JavaScript Object**
```
//Define an object with the Object() prototype
let myCar = new Object();
myCar.maxSpeed = 50;//property
myCar.driver = "Shaun";//property
myCar.drive = function() {//method
    console.log("now driving");
};

myCar.drive(); //calling a method

//Define an object with object literals
let myCar2 = {
    maxSpeed: 70,
    driver: "Net Ninja",
    drive: function(){
        console.log("Now driving");
    }
};
```

## Video 30
**THIS Keyword**
- Refers to whatever object currently owns the space that calls the "this" keyword

## Video 31
**Constructor Functions**
- The constructor function is used with the "new" keyword to copy from a prototype(almost like creating a mold for creating many of the same or similar objects)
- Constructor functions allow you to reuse the same code instead of having to explicitly define all your objects
```
let Car = function(maxSpeed, driver) {
    this.maxSpeed = maxSpeed;
    this.driver = driver;
    this.drive = function(speed, time) {
        console.log(speed * time);
    };
    this.logDriver = function() {
        console.log("driver name is " + this.driver);
    };
}

//Now let's create cars using the constructor function (or...mold)
let myCar = new Car(70, "Ninja Man");//Note the "new" keyword
let myCar2 = new Car(40, "Humpty Dumpty");
let myCar3 = new Car(10, "Shaun");
let myCar4 = new Car(90, "James Bond");
```

## Video 32
**The Date Object**
- Date object for JS
- Has many methods/properties that you can access
- Use the getTime() method to compare dates
```
let birthday = new Date(1985, 0, 15, 11, 13, 25);

console.log(birthday.getMonth());
console.log(birthday.getFullYear());
console.log(birthday.getDate());
console.log(birthday.getDay());
console.log(birthday.getHours());
console.log(birthday.getTime());
```

## Video 33
**The DOM**
- Document Object Model
- Document is the web page(html)
- Every element in the html is an object
- JS works well with objects so use the DOM to interact with html
- Model is a hierarchy of elements/objects
- Everything we can change in a document is a node in the DOM
 - Nodes: elements, text within elements, attributes

## Video 34
**Traversing the DOM**
- Reach nodes in the DOM with JS methods
```
//Notice that "document" is the highest level node
let myContentDivs = document.getElementsByClassName("content");//Parenthesis, so method

let myH2 = myContentDis[1].getElementsByTagName("h2");
```

## Video 35
**Changing Page Content**
```
let myBody = document.getElementsByTagName("body");

myBody[0].innerHTML;//property that returns the entire inner html for the body tag

myBody[0].innerHTML = "<p>I am a paragraph tag</p>"
```

## Video 36
**Changing Element Attributes**
- Use methods to change element attributes
- getAttribute("href") gets the attribute
- setAttribute("class", "pie") sets the attribute
- Note that properties and methods behave differently sometimes

## Video 37
**Changing CSS Styles**
- Set a element's style attribute to change the style
- Use camelCase for changing style PROPERTIES in JS

## Video 38
**Adding Elements to the DOM**
- Step 1, create the element in JS
- Step 2, add the element to the DOM
```
let newLi = document.createElement("li");
let newA = document.createElement("a");

let menu = document.getElementById("main-nav").getElementsByTagName("ul")[0];
menu.appendChild(newLi);
newLi.appendChild(newA);
newA.innerHTML = "Blog";
```

## Video 39
**Removing Elements from the DOM**
- Step 1, grab element that you want to remove
- Step 2, grab the parent element of the element that you want to remove
```
let parent = document.getElementById("main-nav").getElementsByTagName("ul")[0];
let child = parent.getElementsByTagName("li")[0];
let removed = parent.removeChild(child);
```

## Video 40
**Introduction to JavaScript Events**
- Events fire off when users interact with a web page
- Use JS to react to these events in a way that creates an interactive web page experience
- You can use the method addEventListener() to add events
- Each element has event properties
```
let title = document.getElementById("page-title");
title.onClick = function(){
    alert("You clicked me!");
};
title.onmouseOver = function() {
    alert("You hovered your mouse over me ;)");
};
```

## Video 41
**The onClick Event**
- onClick is an element property
- Change css classes on click events to change element styles in response to click events
- Change style properties directly is response to click events

## Video 42
**Window onLoad Event**
- The onLoad event fires after the initial html has completely loaded
- To make sure that JS only fires after the initial HTML has loaded, wrap  your JS in a function and run the function on the window.onLoad event

## Video 43
**JavaScript Timers**
- Use the setTimeout(myFunction, milliseconds) function to add a time event
- Use the setInterval(myFunction, millisecondsd) function to repeatedly call myFunction
- Store setInterval and setTimeout in a variable, then use clearInterval and clearTimeout to stop timers
- Specify an alternating style change in the myFunction to create a slideshow effect

## Video 44
**Accessing Form Elements**
- Access forms in the document via the document.forms.formName property
- Forms have many properties that can be used for creating interactive forms
