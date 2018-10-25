# Java Script:
JavaScript is a high level, interpreted programing language. It is a language which is also characterized as dynamic, weakly typed.
# String Literal:
```
var myName = "your name";
```
"your name" is called a string literal. It is a string because it is a series of zero or more characters enclosed in single or double quotes.
### Escape Sequences in Strings: 
There are two reasons to use escaping characters: First is to allow you to use characters you might not otherwise be able to type out, such as a backspace. Second is to allow you to represent multiple quotes in a string without JavaScript misinterpreting 
```
Code  Output
(\')	single quote
(\")	double quote
(\\)	backslash
(\n)	newline
(\r)	carriage return
(\t)	tab
(\b)	backspace
(\f)	form feed
```
### Concatenating Strings with Plus Operator:
var myStr="This is the start."+" This is the end.";
o/p: This is the start. This is the end.
### Find the Length of a String:
```
var firstName = "Charles"
var l = firstName.length; 
```
o/p : 7 
### Use Bracket Notation to Find the First Character in a String:
```
var firstName = "Charles"
var firstChar = firstName[0]
```
o/p : C
### Store Multiple Values in one Variable using JavaScript Arrays:
```
var sandwich = ["peanut butter", "jelly", "bread"]
```
### Nest one Array within Another Array:
```
var ourArray = [["the universe", 42], ["everything", 101010]];
```
### Access Multi-Dimensional Arrays With Indexes
```JS
var arr = [
  [1,2,3],
  [4,5,6],
  [7,8,9],
  [[10,11,12], 13, 14]
];
arr[3];// equals [[10,11,12], 13, 14]
arr[3][0]; // equals [10,11,12]
arr[3][0][1]; // equals 11
```
### Manipulate Arrays With 
## 1. push()
```
var arr = [1,2,3];
arr.push(4);
arr is now [1,2,3,4]
```
## 2. pop()
```JS
var myArray = [["John", 23], ["cat", 2]];
var removedFromMyArray=myArray.pop(0)
```
o/p : myArray = [["cat",2]];
## 3. shift()
##### pop() always removes the last element of an array. What if you want to remove the first? That's where .shift() comes in. It works just like .pop(), except it removes the first element instead of the last.
```JS
var myArray = [["John", 23], ["dog", 3]];
var removedFromMyArray = myArray.shift(0)
```
o/p: removedFromMyArray=[["John",23]]
## 4. unshift()
##### .unshift() works exactly like .push(), but instead of adding the element at the end of the array, unshift() adds the element at the beginning of the array.
```
var myArray = [["John", 23], ["dog", 3]];
myArray.unshift(["Paul",35]);
o/p: myArray = [["Paul",35],["John",23],["dog",3]]
```
# JavaScript with Functions:
# 1.
```JS
function my()
{
console.log("white horse")
}
my();
```
o/p: white horse
# 2.
```JS
function my(a,b)
{
var c = a+b;

console.log("c")
}
my(1,2);
```
o/p: c = 3;
## 1. Global Scope and Functions:
Variables which are used without the var keyword are automatically created in the global scope.
```
var myGlobal = 10;
oopsGlobal = 5; <----Global variable
```
## 2. Local Scope and Functions
Variables which are declared within a function, as well as the function parameters have local scope. That means, they are only visible within that function.
## Global vs. Local Scope in Functions
```JS
var someVar = "Hat";
function myFun() 
{
  var someVar = "Head";
  return someVar;
}
```
The function myFun will return "Head" because the local version of the variable is present.
## Practice comparing different values
```JS
function compareEquality(a, b) {
  if (a == b) { 
    return "Equal";
  }
  return "Not Equal";
}
compareEquality(10, "10");
```
o/p: Equal.
 because JavaScript performs type conversion from string to number
## Comparison with the Strict Equality Operator
Strict equality (===), unlike the equality operator, which attempts to convert both values being compared to a common type, the strict equality operator does not perform a type conversion. 
## Comparison with the Greater Than Operator 
Like the equality operator, greater than operator will convert data types of values while comparing.
```
5 > 3 // true
7 > '3' // truevar ourArray = [];
var i = 0;
while(i < 5) {
  ourArray.push(i);
  i++;
}
2 > 3 // false
'1' > 9 // falsvar ourArray = [];
var i = 0;
while(i < 5) {
  ourArray.push(i);
  i++;
}
```
### Greater Than Or Equal To Operator
Like the equality operator, greater than or equal to operator will convert data types while comparing.
```
6 >= 6 // true
7 >= '3' // true
2 >= 3 // false
'7' >= 9 // false
```
### Less than Operator
The less than operator (<) compares the values of two numbers. If the number to the left is less than the number to the right, it returns true. Otherwise, it returns false. Like the equality operator, less than operator converts data types while comparing.
```
2 < 5 // true
'3' < 7 // true
5 < 5 // false
3 < 2 // false
'8' < 4 // false
```
### Less Than Or Equal To Operator
Like the equality operator, less than or equal to converts data types.
```
4 <= 5 // true
'7' <= 7 // true
5 <= 5 // true
3 <= 2 // false
'8' <= 4 // false
```
# Build JavaScript Objects
```JS
var cat = {
  "name": "Whiskers",
  "legs": 4,
  "tails": 1,
  "enemies": ["Water", "Dogs"]
};
```
# Accessing Object Properties with Dot Notation
There are two ways to access the properties of an object: dot notation (.) and bracket notation ([]), similar to an array.
Dot notation is what you use when you know the name of the property you're trying to access ahead of time.
Here is a sample of using dot notation (.) to read an object's property:
### 1. dot Notation
```JS
var myObj = {
  prop1: "val1",
  prop2: "val2"
};
var prop1val = myObj.prop1; // val1
var prop2val = myObj.prop2; // val2
```
### 2.Backet Notation
```JS
var myObj = {
  "Space Name": "Kirk",
  "More Space": "Spock",
  "NoSpace": "USS Enterprise"
};
myObj["Space Name"]; // Kirk
myObj['More Space']; // Spock
myObj["NoSpace"]; // USS Enterprise
```
# Updating Object Properties
```JS
var ourDog = {
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};
ourDog.name = "Happy Camper";
```
``Now when we evaluate ourDog.name, instead of getting "Camper", we'll get his new name, "Happy Camper".``
### 1.Add New Properties to a JavaScript Object
```JS
var ourDog = {
  "name": "Camper",
  "legs": 4,
  "tails": 1,
  "friends": ["everything!"]
};
ourDog.bark = "bow-wow";
```
``we can use it like this 
ourDog.bark = "bow-bow";
or,
ourDog["bark"] = "bow-wow";``
##### Now when we evaluate ourDog.bark, we'll get his bark, "bow-wow".
# Delete Properties from a JavaScript Object
```
delete ourDog.bark;
```
# Using Objects for Lookups
If you have tabular data, you can use an object to "lookup" values rather than a switch statement or an if/else chain. This is most useful when you know that your input data is limited to a certain range.
```JS
function phoneticLookup(val) {
  var result = "";
  var lookUp = {
  "alpha":"Adams",
  "bravo":"Boston",
  "charlie":"Chicago",
  "delta":"Denver",
  "echo" :  "Easy",
  "foxtrot":"Frank",
  "": undefined
  }
  result=lookUp[val]
  return result;
}

phoneticLookup("charlie");
// "Chicago"
```
# Testing Objects for Properties
Sometimes it is useful to check if the property of a given object exists or not. We can use the ``.hasOwnProperty(propname)`` method of objects to determine if that object has the given property name. .hasOwnProperty() returns true or false if the property is found or not.
```JS
var myObj = {
  gift: "pony",
  pet: "kitten",
  bed: "sleigh"
};

function checkObj(arg) {
if (myObj.hasOwnProperty(arg) == true)
{
  return myObj[arg];
}
else{
  return "Not Found";
} 
}
checkObj("gift");

//checkObj("gift") should return "pony".
```
# Manipulating Complex Objects
```js
var myMusic = [
  {
    "artist": "Billy Joel",
    "title": "Piano Man",
    "release_year": 1973,
    "formats": [
      "CD",
      "8T",
      "LP"
    ],
    "gold": true
  },

  {
    artist: "name",
    title: "lastName",
    release_year: 2020,
    formats: [
      "land",
      "plot"
    ],
    gold: true
  }
];
myMusic[0].artist // Billy Joel
myMusic[1].artist // name
```
# Accessing Nested Objects
```js
var myStorage = {
  "car": {
    "inside": {
      "glove box": "maps",
      "passenger seat": "crumbs"
     },
    "outside": {
      "trunk": "jack"
    }
  }
};

var gloveBoxContents = myStorage.car.inside["glove box"]
//result: gloveBoxContents = maps
```
# Accessing Nested Arrays
```js
var myPlants = [
  { 
    type: "flowers",
    list: [
      "rose",
      "tulip",
      "dandelion"
    ]
  },
  {
    type: "trees",
    list: [
      "fir",
      "pine",
      "birch"
    ]
  }  
];

// Only change code below this line

var secondTree = myPlants[1].list[1];
// secondTree = pine
```
# Iterate with JavaScript
## 1. While loops
```js
var ourArray = [];
var i = 0;
while(i < 5) {
  ourArray.push(i);
  i++;
}
```
## 2. For loops:
```js
var ourArray = [];
for (var i = 0; i < 5; i++) {
  ourArray.push(i);
}
```
## 3. Nesting For Loops
```js
var arr = [
  [1,2], [3,4], [5,6]
];
for (var i=0; i < arr.length; i++) {
  for (var j=0; j < arr[i].length; j++) {
    console.log(arr[i][j]);
  }
}
// o/p: 
//      1 
//      2 
//      3
//      4 
//      5
//      6 
```
## 4. Do...While Loops
```js
var ourArray = [];
var i = 0;
do {
  ourArray.push(i);
  i++;
} while (i < 5);
//[0, 1, 2, 3, 4]
```
# Generate Random Whole Numbers with JavaScript
Use Math.random() to generate a random decimal.
Use another function, Math.floor() to round the number down to its nearest whole number.
# Use the parseInt Function
The parseInt() function parses a string and returns an integer.
```js
var a = parseInt("007");
// o/p: 7
```
# Use the parseInt Function with a Radix
The parseInt() function parses a string and returns an integer. It takes a second argument for the radix, which specifies the base of the number in the string. The radix can be an integer between 2 and 36.
```js
parseInt(string, radix);
Another Example:
var a = parseInt("11", 2);
//The radix variable says that "11" is in the binary system, or base 2. This example converts the string "11" to an integer 3.
```
# Use the Conditional (Ternary) Operator
The conditional operator, also called the ternary operator, can be used as a one line if-else expression.
```js
condition ? statement-if-true : statement-if-false;
```
```js
function checkEqual(a, b) {
  return a == b? true : false;
}

checkEqual(1, 2);
```
# Use Multiple Conditional (Ternary) Operators
```js
function findGreaterOrEqual(a, b) {
  return (a === b) ? "a and b are equal" : (a > b) ? "a is greater" : "b is greater";
}
```
