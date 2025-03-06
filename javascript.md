## strict mode in java script writeups =>
(1) https://sentry.io/answers/javascript-use-strict/#
(2) https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode

## What is java script variables
i can create a variable by using var , let and const
variable syntax
keyword   | variable name |  assignment operator  | variable value 
var x = 100;
let x = 100;
const x = 100;

## what is diffrence betwen var , let and const
## var => 
redeclare(yes)==> do not show errorr
Access Before Declare(undefinde) 
variable scope drama() [add to window object]
## let => 
redeclare(no) ==> show errorr
Access Before Declare(errorr) 
variable scope drama()
## const => 
redeclare(no) ==> show errorr
Access Before Declare(errorr) 
variable scope drama()

## java script comment
one line comment => // hello
multi-line comment =>
/*
h
e
l
l
o
*/

## Data types
JavaScript has 8 Datatypes
// Numbers:
let length = 16;
let weight = 7.5;

// Strings:
let color = "Yellow";
let lastName = "Johnson";

// Booleans
let x = true;
let y = false;

// Object:
const person = {firstName:"John", lastName:"Doe"};

// Array object:
const cars = ["Saab", "Volvo", "BMW"];

// Date object:
const date = new Date("2022-03-25");

// If condation
if (condation){
  // Block of code
}

// switch case

switch (condation)
{
case 1:
  return 10;
  break;
case 2:
  return 20;
  break;
case 3:
  return 30;
  break;
}



