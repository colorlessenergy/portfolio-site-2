---
layout: project
title: Scope and JavaScript engine
date: 2018-09-24 4:35 -0700
meta: javascript scope and the javascript engine. this article will explain how variables are seen in javascript and how javascript runs your code.
pic: images/javascript.png
tags: ["javascript"]
---

# scope and the JavaScript engine

![javascript]({{ site.baseurl }}/images/javascript.png "javascript")


## variable lifetime

It begins when it is declared and ends at the end of a function if is it in one, if it isn't in a function it is at the end of global context which means when it the page is closed or refreshed


## hoisting

Hoisting means that all function definition and variable declarations are put to the top of the nearest scope.

Function definition are hoisted, variable initialization are not.

which means that function can be used anywhere in your code even before it is defined. only the variable declaration is hoisted not the value.

```javascript
 greet() // hi
 function greet() {
   console.log('hi')
 }
```

why does it do this?

## the javascript engine

before executing the code, the engine reads the entire file and will throw a syntax error if one is found.

* any function will be saved in memory
* variable initializations will not be run, but variable names will be declared

## the execution and creation phase

```javascript
console.log(i);
greet();

var i = 42;

function greet() {
 console.log('hi')
}
```

creation and execution phase

```javascript

// creation phase
var i;

function greet() {
 console.log('hi')
}

// execution phase

console.log(i);
greet();

i = 42;
```

## the global object

All variables and functions are parameters and methods on the global object.

* browser global object is window
* node global object is global

## execution context

Collections of exeuction context is known as the exeuction stacks.

* stack, first in last out
* queue, first in first out


## lexical environment

Determines how variable names are resolved, especially with nested functions. Child functions contain the scope of the parent function even if the parent function has returned.


happy coding :)

Any question feel free to contact me brianmunozdev@gmail.com