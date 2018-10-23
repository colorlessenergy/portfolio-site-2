---
layout: project
title: the concept of dry, don't repeat yourself
date: "2018-08-20 10:00 -0700"
meta: a explanation of the concept dry, don't repeat yourself, in programming.
pic: images/sandwich.png
tags: ["javascript", "programming", "javascript fundamentals", "web programming", "es6"]
---

# a explanation of the concept dry, don't repeat yourself, in programming.

![picture of a sandwich to demonstrate dry]({{ site.baseurl }}/images/sandwich.png "picture of a sandwich to demonstrate dry")

## what is DRY

DRY stands for don't repeat yourself. This way of programming is really powerful because you will end up with maintainable and readable code.

## an example on how to use DRY

first I am going to show you without following the principles of DRY.

lets says we are making sandwiches and for every sandwiches we need 3 different variable declarations to store the different foods that will go on the sandwich. the variables will store the bread type, condiment, and type of meat.

```javascript

let bread = "whole wheat";
let condiment = "honey mustard";
let meat = "turkey";

let sandwich = bread + condiment + meat + bread;

```

now lets say we want a different sandwich and want to keep the sandwich we made before, we will have to make new variables to store the different breads, condiments and meat.

```javascript
let bread = "whole wheat bread";
let condiment = "honey mustard";
let meat = "turkey";

let bread2 = "oat bread";
let condiment2 = "mustard";
let meat2 = "ham";

let sandwich = bread + condiment + meat + bread;
let sandwich2 = bread2 + condiment2 + meat2 + bread2;
```

this is a bad idea because everytime we want a new sandwich we are going to make new variables to store all the items we need to make a sandwich. We could use a function and pass in the three different items as arguments for what we want on the sandwich. This way we won't repeat the code but call the function when ever we want a new sandwich.

```javascript

// call this function when ever you want to make a new sandwich
function sandwich(bread, condiment, meat) {
  return bread + condiment + meat + breadType
}


// now we give the function call the values we would of stored in the variables
let sandwich = sandwich("whole wheat bread", "honey mustard", "turkey");
let sandwich2 = sandwich("oat bread", "mustard", "ham");
```

This looks cleaner and is less code then before which makes it easier to read and easier to maintain.

## the concept

the concept of don't repeat yourself is very simple if you ever find yourself writing the same code more than once think about how you could put it into a function and call that function instead of having to write the same code. This reduces bugs because you don't have to remember all the locations you duplicated the code because it will be in a function.

happy coding :)
