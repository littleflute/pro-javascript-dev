v0.2.1<br>
[..](..)<br>

Chapter01 [Chapter02](Chapter02) [Chapter03](Chapter03) [Chapter04](Chapter05) [Chapter02](Chapter05) [Chapter06](Chapter06)    

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
