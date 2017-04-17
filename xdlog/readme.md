v1.1.0
[Chapter 1](Chapter01)
[Chapter 2](Chapter02)
[Chapter 3](Chapter03)
[Chapter 4](Chapter04)
[Chapter 5](Chapter05)
[Chapter 6](Chapter06)
[Chapter 7](Chapter07)
[Chapter 8](Chapter08)
[Chapter 9](Chapter09)
[Chapter 10](Chapter10)
[Chapter 11](Chapter11)


javascript test

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
