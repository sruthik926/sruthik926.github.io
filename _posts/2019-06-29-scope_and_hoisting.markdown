---
layout: post
title:      "Scope & Hoisting"
date:       2019-06-29 14:48:37 +0000
permalink:  scope_and_hoisting
---

This blog is going to discuss two important concepts of JavaScript - Scope and Hoisting. 

Scope is all about where variables and functions are currently placed and it’s accessibility. This is a general definition of scope. However, within JS, there are different types of scope. I am going to give a breakdown of few types if scope. 

Global scope 

- - if a variable is declared and assigned outside of a function, then it globally scoped. (Example 1 demonstrates this)

**Example 1 **

var emotion = "I am happy";

function one(){
  console.log(emotion);
}

one(); /* Prints I am happy */


When function one is invoked, ‘I am happy’ is printed on the console. We are able to access the variable emotion within the function because emotion is within the global scope.

Global scope can also be applied to functions.  Functions that are not within any block or function is within the global scope or global execution context. In other words, these global variables or functions can be accessed from anywhere within the JS code.


Local scope

This means limited access of variables and functions. Variables or functions placed within a function are locally scoped. . Those variables or functions are really only accessible within those functions. (Example 2 ) 


**Example 2**

function computerProg(){
  var c = "I love to program";
  console.log(c);

} 

computerProg();

console.log(c);

if we run this on JS console, we would get an error message “VM821:9 Uncaught ReferenceError: c is not defined
    at <anonymous>:9:13”
**

With var, variables can be reassigned and redeclared.  However,  this will not result in an error.  This can get confusing within a larger application. Therefore, It's not recommended to use var. 

Block Scope - 
Block level scope was introuced in javascript in the ES6 specification to align js with a feature that was available in most other popular languages like C++ and Java. Let and const are new features of ES6.  Variables declared with let within a  block   canot be referenced outside the block - {}  - For example

**Example 3 **

if(true){
 let a = “Flatiron Student”;
}
console.log(a); 

We get the following error we type the 2nd if block on the JS console.

VM88:4 Uncaught ReferenceError: a is not defined
    at <anonymous>:4:13


Hoisting 

The dictionary meaning of hoisting is "an act of raising or lifting."  Hoisting, within JS, means 'raising or lifting' variable & function declarations to the top of current scope.

For example,
  
  - sayHi();

Function sayHI(){
   return ‘Hi guest! Welcome.’;
}

This stilll works - and prints out :Hi guest! Welcome!’ though we are invoking the function before declaraitng it. Due to hoisting - this declaration goes to top. This is becuase, during the compliation phase hoisting facilitates moving the function to the top of the memory storage. Variable declarations are also hoisted. However, there are few differences between let and var when they are hoisted.   The initialization value is undefined in var. For example

function eatPizza(){
  console.log(pizza)
   var pizza = “I love pizza”;
}

Although the var pizza is hoisted it is undefined and hence the console.log will print "undefined".

However, let works differently when  hoisted. Variables declared with let cannot be referenced prior to initialization and will result in the following error - “ERROR: Uncaught ReferenceError: myVar is not defined”. ES6 recommends usage of let. var is no longer recommended.

Hope this blog serves as a basic introduction to scope and hoisting in javascript for newcomers to web development.

Sources Used

"https://www.merriam-webster.com/dictionary/hoist"
https://dev.to/sarah_chima/var-let-and-const--whats-the-difference-69e
https://learn.co/tracks/full-stack-web-development-v6/javascript/principles/hoisting
https://learn.co/tracks/full-stack-web-development-v6/javascript/principles/scope





