### 1.What are the different data types present in javascript?
- there are two types primitive and non-primitive data-types 
- to know the type of dataType we can use typeOf operator
#### Primitive :
- String
- Number
- BigInt
- boolean
- Undefined
- Null
- Symbol
#### Non-primitive
- Object
### 2.  Explain Hoisting in javascript.
- Hoisting is the default behaviour of javascript where variables and functions are moved on top of the their respective scope
```javascript
x=5; 
var x;
console.log(x) // output is 5
```
```javascript
foo() // output is helloo
function  foo(){
    console.log("helloo")
}
```
```javascript
console.log(x) // output is undefined
x=5;
var x
```
### 3. Why do we use the word “debugger” in javascript?
- The debugger for browser is activated in order to debug the code
### 4. Difference between “ == “ and “ === “ operators.
- == it checks the value where === checks their value and also their datatype
```javascript
var x= 10;
var y = '10'
if(x==y){
    console.log('x==y')
}
if(x===y){
    console.log('x===y')
}
// output is x==y
```
### 5. Difference between var and let keyword in javascript.
- var and let are used to declare variables however there is difference in their scope, hoisting, redeclaration
#### Scope :
- variables declared with var have function scope they have global scope
- variables declared with let have block scope
#### hoisting :
- var : they are hoisted to the top of their scope
- let : let variables are also hoisted 
#### Redeclaration :
- var : variables are redeclared within the same scope
- let : variables  cannot be redeclared within the same scope
### 6. Explain Implicit Type Coercion in javascript.
- Implicit Type Coercion in javascript is the automatic coercion from one datatype to another
```javascript
var x=3;
var y= '3'
console.log(x+y);
//output is 33 here y value is string but it converts to number
```
###  7.  Is javascript a statically typed or a dynamically typed language?
- JavaScript is dynamically typed language because type of variable is checked at run-time
### 8. What is NaN property in JavaScript?
- NaN property represents not a number . it indicates a value that it is not a legal number
```javascript
console.log(isNaN('helloo')) // true
console.log(isNaN(45)) //false
```
### 9. Explain passed by value and passed by reference.
- in javascript primitive data-types are follows  passed by value and non-primitive data types follows passed by reference
- When a variable is passed by value it creates a copy of the variable's value is made and passed to the function .
- Any modifications made to the parameter within the function do not affect the original variable.
- When a variable is passed by reference, the reference or memory address of the variable is passed to the function. 
- Changes made to the parameter within the function will affect the original variable.
### 10.  What is an Immediately Invoked Function in JavaScript?
- An immediately invoked function expression (IIFE) is a javascript function that is executed immediately after it is defined
- the syntax for IIFE is 
- it is way to create a function scope and execute code in that scope without polluting the global scope
```javascript
(function(){
    console.log("helllo")
})();
```
### 11. What do you mean by strict mode in javascript and characteristics of javascript strict-mode?
- In ECMASCRIPT 5 new feature called javascript  strict mode is introduced 
- it makes the variables, functions work on strict mode
#### Characteristics of strict mode
- duplicate arguments are not allowed
- in strict mode javascript keywords are not allowed to use as arguments or function name
- developers will not allowed to create global variables
- The 'use strict' keyword is used to define strict mode at the start of the script. Strict mode is supported by all browsers
### 12. Explain Higher Order Functions in javascript.
- A function which takes another function as argument or a function which returns another function is called higher order function
- Higher order functions are called First class citizens in javascript
```javascript
function A(){
    return (function (){
        console.log("inner function")
    })
}
var x= A();
// A function which returns other function 
```
```javascript
function B(A){
    A()
}
B( function A(){
    console.log("from anonymous function")
} )
//A function which takes another function as arguments
```
### 13. What is the difference between exec () and test () methods in javascript?
- Both are regular expressions methods used in javascript 
- exec() : it is used to search a string in specific pattern if it finds it return the pattern or else it return the empty result
- test() : it is used to find the string in specific pattern if it finds it return true or else false
### 14. What is currying in JavaScript?
- currying is a advanced technique in javascript which transform function of arguments n , to n functions of one or fewer arguments
```javascript
function add (a) {
    return function(b){
        return a + b;
    }
}

add(3)(4) 
```
### 15. Explain Closures in JavaScript.
### 16.  What is a Temporal Dead Zone?
- Temporal Dead Zone is a behaviour in javascript that occurs when variable is declared with let or const are accessed before they are assigned a value
```javascript
x=5;
let x; 
console.log(x) // it give reference error  Cannot access 'x' before initialization
```
### 17.  Explain call(), apply() and, bind() methods.
### 18. What are callbacks?