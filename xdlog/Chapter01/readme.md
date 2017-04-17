v2.6.13<br>
[..](..)<br>

Chapter01 [Chapter02](Chapter02) [Chapter03](Chapter03) [Chapter04](Chapter05) [Chapter02](Chapter05) [Chapter06](Chapter06)    


<style>
span.highlight {
    background-color: blue;
}
</style>

Listing1-1.js
```js
var house = {
    rooms: 7,
    sharedEntrance: false,
    lock: function() {},
    unlock: function() {}
};

// Read out the values of the two properties
alert(house.rooms); // 7
alert(house.sharedEntrance); // false

// Execute the ‘lock’ method of the object
house.lock();

// Update the value for the ‘rooms’ property
house.rooms = 8;

// Add a completely new property dynamically
house.floors = 2;

// Read out the ‘rooms’ property again – notice it has now changed
alert(house.rooms); // 8
```
Listing1-2.js
```js
// Define a constructor called Accommodation
function Accommodation() {}

// Assign properties to our "class" blueprint
Accommodation.prototype.floors = 0;
Accommodation.prototype.rooms = 0;
Accommodation.prototype.sharedEntrance = false;

// Assign methods to our "class" blueprint
Accommodation.prototype.lock = function() {};
Accommodation.prototype.unlock = function() {};

// Create object instances from our Accommodation "class"
var house = new Accommodation();
var apartment = new Accommodation();

// Read properties from object instances
alert(house.floors); // 0
alert(house.sharedEntrance); // false

// Write properties to object instances to set the correct values
house.floors = 2;
accommodation.sharedEntrance = true;

// Execute methods on object instances
house.unlock();
apartment.lock();
```
Listing1-3.js
```
// Define a constructor called Accommodation
function Accommodation() {}

// Assign properties and methods to our "class" blueprint with an object literal
Accommodation.prototype = {
    floors: 0,
    rooms: 0,
    sharedEntrance: false,
    lock: function() {},
    unlock: function() {}
};

// Create object instances from our Accommodation "class"
var house = new Accommodation();
var apartment = new Accommodation();

// Read properties from object instances
alert(house.floors); // 0
alert(house.sharedEntrance); // false

// Write properties to object instances to set the correct values
house.floors = 2;
accommodation.sharedEntrance = true;

// Execute methods on object instances
house.unlock();
apartment.lock();
```
Listing1-4.js
```js
// Define a constructor called Accommodation
function Accommodation() {}

// Assign properties and methods to our "class" blueprint with an object literal
Accommodation.prototype = {
    floors: 0,
    rooms: 0,
    sharedEntrance: false,
    lock: function() {},
    unlock: function() {}
};

// Create an object instance
var house = new Accommodation();

// Dynamically add a new method to the "class" prototype
Accommodation.prototype.alarm = function() {};

// The existing object instance gains the new method automatically
house.alarm();
```
<div style="border:1px red solid;">Listing1-5.js</div>
```js
// Variable declared outside of any function is in global scope and available to access anywhere
var myLibrary = {
    myName: "Dennis"
};

function doSomething() {
    // Variable declared within a function is not accessible outside that function
    var innerVariable = 123;

    // The global variable is accessible from within the function
    myLibrary.myName = "Hello";

    function doSomethingElse() {
        // Variables declared in a surrounding scope are accessible
        innerVariable = 1234;
    }

    doSomethingElse();

    alert(innerVariable); // 1234
}

doSomething();

// This property was overridden within the doSomething function
alert(myLibrary.myName); // "Hello"

// Trying to access a variable declared within a function from outside results in an error
alert(innerVariable); // ERROR!
```
<span class="highlight">Listing1-6.js</span>
```js
// Outside of any function, ‘this’ represents the global ‘window’ object
alert(this === window); // true

// Because the doSomething function is called outside of an object, the keyword this adopts
// the global JavaScript window object in the browser.
function doSomething() {
    alert(this === window); // true
}

doSomething();

var house = {
    floors: 2,
    isLocked: false,
    lock: function() {
        alert(this === house); // true, as the this keyword represents the object containing this method

        // We can treat ‘this’ as equivalent to the ‘house’ object, including using dot notation
        this.isLocked = true;
    }
};

house.lock();

alert(house.isLocked); // true
```

 
 <button onclick="myFunction()">Try it 1</button>
<script>
function myFunction() {
    var x = document.getElementById("header");
    x.getElementsByClassName("fork")[0].style.backgroundColor = "yellow";
    x.getElementsByClassName("fork")[0].style.border = "1px solid red"; 
     
    document.getElementsByTagName("h1")[0].innerHTML = "Chapter 01";
}


</script>


