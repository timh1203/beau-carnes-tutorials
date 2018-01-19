#JavaScript Basics (complete course)
[View full playlist here](https://www.youtube.com/playlist?list=PLWKjhJtqVAbk2qRZtWSzCIN38JC_NdhW5)

## 1. Variables ✔️
### Variables are containers for storing data values. This video also covers naming conventions.
12/23/2017

## 2. Data Types ✔️️
### The seven data types in JavaScript are boolean, null, undefined, number, string, symbol, and object.
12/23/2017

```js
// JS Nuggets: Data Types

// There are 7 data types

// Boolean. true and false

var data = true;

if (data) {
  console.log("Booleans rule!")
} else {
  console.log("Booleans are lame.")
}

// null. is an assignment value that means “no value”

var n = null;
console.log(n * 32);

// undefined. means a variable has not been declared, or has been declared but has not yet been assigned a value

var a;
console.log(a + 2);

// Number. 42 or 3.14159.

var num = 3.6;
var ber = 6.4;
console.log(num + ber);

// String. "Hey!"

var name = "Beau";
console.log("Hi! My name is " + name);

// Symbol (new in ECMAScript 2015). A data type whose instances are unique and immutable.

var sym1 = Symbol("foo");
var sym2 = Symbol("foo");
console.log(sym1 === sym2)
console.log(String(sym1) === String(sym2))

// Object - An object is a collection of properties, and a property is an association between a name (or key) and a value.

var myCar = new Object();
myCar.make = "Ford";
myCar.model = "Mustang";

console.log(myCar.make);
```

## 3. Numbers ✔️️
### Working with numbers including adding, subtracting, multiplying, dividing, modulus, increment, decrement, and compound assignment.
12/23/2017

## 4. String Basics ✔️️ 
### Strings are a group of characters.
12/23/2017

```js
var myName = 'Beau';

var sentence = "He said \"Hi!\""; // He said Hi!
var sentence = 'He said "Hi!"'; // He said Hi!

/*
Code	Output
\'	single quote
\"	double quote
\\	backslash
\n	newline
\r	carriage return
\t	tab
\b	backspace
\f	form feed
*/

var fullName = 'Beau ' + 'Carnes';  // 'Beau Carnes'

var sentence2 = 'My name is ' + fullName; // 'My name is Beau Carnes'

fullName += ' is my name.'; // 'Beau Carnes is my name'
```

## 5. Strings: bracket notation ✔️️
### Bracket notation allows you to access a specific character in a string.
12/23/2017

## 6. 20 String Methods in 7 Minutes
### String methods featured in this video: charAt, charCodeAt, concat, endsWith, fromCharCode, includes, indexOf, lastIndexOf, match, repeat, replace, search, slice, split, startsWith, substr, substring, toLowerCase, toUpperCase, trim.
12/24/2017

- `slice` and `match` returns arrays

```js
/* 20 String Methods */

var stringOne = "freeCodeCamp is the best place to learn"
var stringTwo = "frontend and backend development"

// charAt()
console.log(stringOne.charAt(1))

// charCodeAt()
console.log(stringOne.charCodeAt(1))

// concat()
console.log(stringOne.concat(stringTwo))

// endsWith()
console.log(stringOne.endsWith("to"))

// fromCharCode()
console.log(String.fromCharCode(114))

// includes()
console.log(stringTwo.includes("end"))

// indexOf()
console.log(stringTwo.indexOf("end"))

// lastIndexOf()
console.log(stringTwo.lastIndexOf("end"))

// match()
console.log(stringTwo.match(/end/g))

// repeat()
console.log(stringOne.repeat(3))

// replace()
console.log(stringTwo.replace(/end/g, "END"))

// search()
console.log(stringTwo.search("end"))

// slice()
console.log(stringTwo.slice(2, 4))

// split()
console.log(stringOne.split(" "))

// startsWith()
console.log(stringOne.startsWith("free"))

// substr()
console.log(stringTwo.substr(2, 4))

// substring()
console.log(stringTwo.substring(2, 4))

// toLowerCase()
console.log(stringOne.toLowerCase())

// toUpperCase()
console.log(stringOne.toUpperCase())

// trim()
var stringThree = "     Subscribe now!      ";
console.log(stringThree.trim())
```

## 7. Functions ✔️️
### Functions are one of the fundamental building blocks in JavaScript. This video covers function definitions, names, arguments, parameters, scope, and nesting functions.
12/24/2017

```js
/* Functions */

function square(number) {
  return number * number;
}

console.log(square(4));

var someVar = "Hat";
function myFun() {
  var someVar = "Shoes";
  console.log(someVar);
}

myFun();
console.log(someVar);

console.log(addSquares(1, 3));

function addSquares(a, b) {
  function square(x) {
    return x * x;
  }
  return square(a) + square(b);
}

a = addSquares(2, 3); // returns 13
b = addSquares(3, 4); // returns 25
c = addSquares(4, 5); // returns 41
```

## 8. Hoisting ✔️️
### Hoisting is when variable and function declarations are processed before any code is executed.
12/24/2017

```js
// JS Nuggets
// Hoisting

// console.log(notDeclared); // Uncaught ReferenceError: notDeclared is not defined

console.log(definedLater);
var definedLater;
definedLater = 'I am defined!'
console.log(definedLater)


console.log(definedSimulateneously);
var definedSimulateneously = 'I am defined!'
console.log(definedSimulateneously)


doSomethingElse();
function doSomethingElse(){
  console.log('I did it!');
}


functionVar(); // Uncaught TypeError: functionVar is not a function
var functionVar = function(){
  console.log('I did it!');
}
```

## 9. Comparison Operators & If Else ✔️️
### Comparison operators like >, <, =>, and =<. Also, use if / else statements to execute a block of code if a specified condition is true.
12/24/2017

```js
/** Comparison Operators & If... Else **/

var isFCCGreat = true;

if (isFCCGreat) {
  console.log("Free Code Camp is amazing!");
} else {
  console.log("Free Code Camp is horrible!");
}; 

// Comparison Operators: > < <= >= == !=

var age = 10;

if (age >= 18) {
  console.log("You are an adult!");
} else if (age < 2) {
  console.log("You are a baby!");
} else if (age < 18) {
  console.log("You are a child!");
};

if (age != 18) {console.log("You are NOT eighteen.")};
```

## 10. == vs === ✔️️
### Differences between abstract and strict equality.
12/24/2017

```js
// JS Nuggets: == vs ===

// == abstract equality

// === strict equality

console.log(3 == "3"); // true
console.log(3 === "3"); // false

console.log(true == '1'); // true
console.log(true === '1'); // false

console.log("This is a string." == new String("This is a string.")); // true
console.log("This is a string." === new String("This is a string.")); // false
```

## 11. Null vs Undefined ✔️️
### Differences between null and undefined.
12/26/2017

```js
// JS Nuggets: Null vs Undefined

var test
console.log(test)

test = null

console.log(test)

console.log(typeof null)
console.log(typeof undefined)
console.log(null === undefined)
console.log(null == undefined)
console.log(null === null)
console.log(null == null)
console.log(!null)
console.log(!!null)
console.log(1 + null)
console.log(1 + undefined)
```

## 12. Logical operators && TRICKS with short-circuit evaluation 
### Logical operators are ‘and’ (&&) and ‘or’ (||). These also allow you to do some tricks using short-circuit evaluation.
12/26/2017

```js
// JS Nuggets: Short-circuit Evaluation
if ( 4 > 5 && 5 > 6 ) {
  console.log("hi")
} else {
  console.log("no")
}

var test = true;
var isTrue = function(){
  console.log('Test is true.');
};
var isFalse = function(){
  console.log('Test is false.');
};

if(test){
//  isTrue();
}

( test && isTrue() );


test = false;
if(!test){
  isFalse(); 
}

( test || isFalse());



function theSameOldFoo(name){ 
  name = name || 'Bar' ;
  console.log("My best friend's name is " + name);
}
theSameOldFoo(); 
theSameOldFoo('Beau'); 
```

## 13. Ternary Operator ✔️️
### The ternary operator, or conditional operator, takes three arguments and is basically a shortened way of writing an if-else statement.
12/26/2017

```js
// JS Nuggets: Ternary Operator

// condition ? expr1 : expr2

var age = 15;

if (age >= 18) {
	console.log("You are an adult!");
} else {
	console.log("You are a kid");
};

console.log((age >= 18) ? "You are an adult!" : "You are a kid.");

var stop;

age > 18 ? (
    console.log("OK, you can go."),
    stop = false
) : (
    console.log("Sorry, you are much too young!"),
    stop = true
);

var firstCheck = false,
    secondCheck = false,
    access = firstCheck ? "Access denied" : secondCheck ? "Access denied" : "Access granted";

console.log(access);
```

## 14. Switch Statements ✔️️
### Control the flow of your program with switch statements.
12/26/2017

```js
// JS Nuggets: Switch Statements

let day;
switch (new Date().getDay()) {
    case 0:
    	day = "Sunday";
        break;
    case 1:
    	day = "Monday";
        break;
    case 2:
    	day = "Tuesday";
        break;
    case 3:
    	day = "Wednesday";
        break;
    case 4:
    	day = "Thursday";
        break;
    case 5:
    	day = "Friday";
        break;
    case 6:
    	day = "Saturday";
}
console.log(day)


var Animal = 'chicken';
switch (Animal) {
  case 'Cow':
  case 'Giraffe':
  case 'Dog':
  case 'Pig':
    console.log('This animal will go on Noah\'s Ark.');
    Break;
  case 'Spoon':
    console.log('A spoon is not an animal!');
    break;
  case 'Dinosaur':
  default:
    console.log('This animal will not be on the Ark.');
}
```

## 15. Arrays ✔️️
### Arrays are ways to store more than one value in a single variable. This video also covers nested arrays and the forEach method.
12/26/2017

```js
/* Array Basics */

var sandwich = ["peanut butter", "jelly", "bread"];

var teams = [["Bulls", 23], ["White Sox", 45]];

console.log(sandwich[1]);

sandwich[1] = "bananas";
console.log(sandwich);

console.log(teams[1][0]);
teams[1][0] = "red socks";
console.log(teams);

sandwich.forEach(function(element) {
    console.log(element);
});
```

## 16. Common Array Method
### Learn how to use 10 different array methods: push, pop, concat, join, reverse, shift, unshift, sort, slice, and splice.
1/8/2018

```js
// JS Nuggets: 10 Common Array Methods

var arr = ["a", "b", "c"];

arr.push("d");
console.log(arr);

console.log(arr.pop());
console.log(arr);

var arr2 = ["g", "q"];
console.log(arr.concat(arr2));
console.log(arr2);

console.log(arr.join("!"));

console.log(arr.reverse());
console.log(arr);

console.log(arr.shift());
console.log(arr);

console.log(arr.unshift("p"));
console.log(arr);

console.log(arr.slice(1,3));

arr.push("i");
arr.push("f");
arr.sort(arr);
console.log(arr);

console.log(arr.splice(2, 2, "JS Nuggets"));
console.log(arr);
```

## 17. Copying Arrays (deep and shallow)
### Shallow copy arrays using slice and the spread operator. Deep copy arrays using JSON.stringify.
1/8/2018

```js
/* Copying Arrays */

var original = [true, true, undefined, false, null];

// slice
var copy1 = original.slice(0);


// spread operator
var copy2 = [...original];
console.log(copy1, copy2);


// DEEP copying
var deepArray = [["freeCodeCamp"]];
var shallowCopy = deepArray.slice(0);

shallowCopy[0].push("is great");
console.log(deepArray[0], shallowCopy[0])

var deepCopy = JSON.parse(JSON.stringify(deepArray));

deepCopy[0].push("is great");
console.log(deepArray[0], deepCopy[0])
```

## 18. Random numbers & parseInt️️️️ ✔ ️ ️
### Create random numbers! Also, use parseInt to convert strings to integers.
1/8/2018

```js
/* Random numbers & parseInt */

// console.log(Math.floor(Math.random() * 20));

function randomRange(min, max) {

  return Math.floor(Math.random() * (max - min + 1)) + min;
}

console.log(randomRange(1, 9));


console.log(parseInt("11", 2));
```

## 19. For Loops ✔
### For loops are one of the most common ways to repeat things in JavaScript.
1/10/2018

```js
/* For Loops */

// for ([initialization]; [condition]; [final-expression]) {}

var ourArray = [];
for (var i = 0; i < 5; i++) {
  if (i > 2) break;
  ourArray.push(i);
}
console.log(ourArray);

var arr = [10,9,8,7,6];
for (var i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}

var arr = [
 [1,2], [3,4], [5,6]
];
for (var i=0; i < arr.length; i++) {
 for (var j=0; j < arr[i].length; j++) {
   console.log(arr[i][j]);
 }
}
```

## 20. While / Do While ✔
### While and do… while are ways to loop over code in JavaScript.
1/10/2018

```js
/* While, Do While */

var n = 0;

while (n < 5) {
  n++;
  
  if (n == 3) break;
  console.log("n = " + n);
}

var i = 0;

do {
  i++;
  console.log("i = " + i);
} while (i < 5);

// &turn_off_js=true
```

## 21. For in / For of
### For… in and for… of loops allow you to loop through property names and values in JavaScript.
1/10/2018

```js
/* for... in / for... of */

// usage

// for (variable in object) {
//   statements
// }

// for (variable of object) {
//   statement
// }

let person = {fname:"Beau", lname:"Carnes", arms:2}; 

let arr = [3, 5, 7];
arr.foo = 'hello';

let text = "";
for (let x in person) {
  text += person[x];
  console.log(x);
};
console.log(text);

for (let i in arr) {
  console.log(i);
};

for (let i of arr) {
  console.log(i);
};

```

## 22. Array Iteration: 8 Methods
### Learn eight methods to iterate through an array in JavaScript! Methods include: forEach, map, filter, reduce, sum, every, find, findIndex.
1/10/2018

```js
// JS Nuggets
// Array iteration: 8 methods

// forEach
[1, 2, 3].forEach(function (item, index) {
  console.log(item, index);
});


// map
const three = [1, 2, 3];
const doubled = three.map(function (item) {
  return item * 2;
});
console.log(doubled);


// filter
const ints = [1, 2, 3];
const evens = ints.filter(function (item) {
  return item % 2 === 0;
});
console.log(evens);


// reduce
const sum = [1, 2, 3].reduce(function (result, item) {
  return result + item;
}, 0);
console.log(sum)


// some
const hasNegativeNumbers = [1, 2, 3, -1, 4].some(function (item) {
  return item < 0;
});
console.log(hasNegativeNumbers);


// every
const allPositiveNumbers = [1, 2, -3].every(function (item) {
  return item > 0;
});
console.log(allPositiveNumbers);


// find
const objects = [{ id: 'a' }, { id: 'b' }, { id: 'c' }];
const found = objects.find(function (item) {
  return item.id === 'b';
});
console.log(found);


// find index
const objects2 = [{ id: 'a' }, { id: 'b' }, { id: 'c' }];
const foundIndex = objects2.findIndex(function (item) {
  return item.id === 'b';
});
console.log(foundIndex)
```

## 23. Objects
### Objects are stand-alone entities with properties and types.
1/10/2018

```js
// JS Nuggets: Objects

var myCar = new Object();
myCar.make = "Ford";
myCar.model = "Mustang";
myCar.color;
console.log(myCar.make);
console.log(myCar.color);

myCar["year"] = 1969;
console.log(myCar["model"])

myCar["Do I like?"] = "I hate my car.";
console.log(myCar["Do I like?"]);



function showProps(obj, objName) {
  var result = "";
  for (var i in obj) {
    // obj.hasOwnProperty() is used to filter out properties from the object's prototype chain
    if (obj.hasOwnProperty(i)) {
      result += objName + "." + i + " = " + obj[i] + "\n";
    }
  }
  return result;
}
console.log(showProps(myCar, "myCar"));

// Creation: object initializer
var myHonda = {color: "red", wheels: 4, engine: {cylinders: 4, size: 2.2}};

// Creation: constructor function
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}

var mycar = new Car("Chevy", "Malibu", 1993);
var anothercar = new Car("Mazda", "Miata", 1990);
console.log(mycar.model);
mycar.color = "black";
console.log(mycar.color);

// Creation: Object.create
var Animal = {
  type: "Invertebrates", 
  displayType: function() {  
    console.log(this.type);
  }
}

var animal1 = Object.create(Animal);
animal1.displayType(); 

var fish = Object.create(Animal);
fish.type = "Fishes";
fish.displayType();
```

## 24. Objects, part 2
### Learn more about objects. This video covers using objects for lookups, removing properties using delete, testing for properties, accessing and modifying nested objects, and creating an array of all object keys.
1/10/2018

```js
// NEED TO TYPE IN THE CODE
```

## 25. AJAX
### AJAX in allows allows you to update parts of a web page without reloading the entire page.

```js

```

## 26. JSON
### JSON stands for JavaScript Object Notation. It is a syntax for storing and exchanging data.

```js

```

## 27. this
### The keyword ‘this’ refers to the object that “owns” the JavaScript code.

```js

```

## 28. Closures
### A closure is the combination of a function and the environment where the function is declared.

```js

```
## 29. Promises
### A promise represents the eventual result of an asynchronous operation.

```js

```

## 30. Desktop Notifications
### The Notifications API lets a web page or app send notifications that are displayed outside the page at the system level. This lets web apps send information to a user even if the application is idle or in the background.

```js

```

## 31. Immediately Invoked Function Expression
### An Immediately Invoked Function Expression (IIFE) is a JavaScript function that runs as soon as it is defined.

```js

```

## 32. Strict Mode
### “use strict” — Strict mode in JavaScript tightens the rules for certain behaviors. You can execute JavaScript code in strict mode by using the “use strict” directive.

```js

```

## 33. Check if a property is in an object
###How do you check if a property is in an object in JavaScript? Learn three ways in this video. Two of the ways are ‘in’ and ‘hasOwnProperty’.

```js

```

## 34. setInterval and setTimeout: timing events
### setTimeout and setInterval are timing events in JavaScript that both allow execution of code at specified time intervals. This quick tutorial shows how to use them.

```js

```

## 35. try, catch, finally, throw — error handling in JavaScript
### Error handling in JavaScript uses the keywords: try, catch, finally, and throw.

```js

```

## 36. Dates
### Work with dates in JavaScript.

```js

```

#ES6 Basics (complete course)
[View full playlist here]()
/////
///// Var vs Const vs Let —Three different ways to declare variables.
/////
// JS Nuggets: Const vs Let vs Var

// const - for values that never change

const Pi = 3.14
// Pi = 1 //error
console.log(Pi);


// let - for block-level variables

for(let i = 0; i < 3; i++) {
  console.log(i);
}
// console.log(i) //error


// var - for variables available to entire function or program

console.log(j)
for(var j = 0; j < 3; j++) {
  console.log(j);
}
console.log(j)

/////
///// Classes — Learn about class expressions, class declarations, and inheritance / extending.
/////
//**JS Nuggets: Classes**

//**class declaration**
class Person {
  constructor(name, year_born) {
    this.name = name;
    this.year_born = year_born;
  }
  
  get age() {
    return this.calcAge();
  }

  calcAge() {
    return new Date().getFullYear() - this.year_born;
  }
  
  what() {
    console.log(this.name + ' is a person.');
  }
  
  static arms() {
    return 2;
  }
}

var me = new Person("Beau", 1983);
console.log(me.name + " was born in " + me.year_born + "!")
me.what();
console.log(me.name + " has " + Person.arms() + " arms!")

class Juggler extends Person {
  what() {
    super.what();
    console.log(this.name + " is a juggler.");
  }
}

var you = new Juggler ("Jay", 1980);
me.what();
you.what();


//**class expressions**
// unnamed
var Person2 = class {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
};

// named
var Person3 = class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
};

/////
///// Symbols —Symbols are a unique immutable data type.
/////
// JS Nuggets: Symbols

// Creation

let symbol1 = Symbol('symbol2');
let symbol2 = Symbol('symbol2');
console.log(symbol1 === symbol2);
console.log(typeof symbol1);
console.log('symbol: ' + symbol1.toString());


// Use case 1: Symbols as property keys
   const MY_KEY = Symbol();
    let obj = {};
    
    obj[MY_KEY] = 123;
    console.log(obj[MY_KEY]);


// Use case 2: constants representing concepts
const COLOR_RED    = Symbol('Red');
const COLOR_ORANGE = Symbol('Orange');
const COLOR_YELLOW = Symbol('Yellow');
const COLOR_GREEN  = Symbol('Green');
const COLOR_BLUE   = Symbol('Blue');
const COLOR_VIOLET = Symbol('Violet');

function getComplement(color) {
    switch (color) {
        case COLOR_RED:
            return COLOR_GREEN;
        case COLOR_ORANGE:
            return COLOR_BLUE;
        case COLOR_YELLOW:
            return COLOR_VIOLET;
        case COLOR_GREEN:
            return COLOR_RED;
        case COLOR_BLUE:
            return COLOR_ORANGE;
        case COLOR_VIOLET:
            return COLOR_YELLOW;
        default:
            throw new Exception('Unknown color: '+color);
    }
}

/////
///// Template Literals — Template literals are string literals allowing embedded expressions. These are surrounded by backticks ``.
/////