---
layout: post
title:      "call() vs apply() vs bind()"
date:       2018-09-05 13:57:24 -0400
permalink:  call_vs_apply_vs_bind
---


Moving into the JavaScript portion of the curriculum, I came to realize how incredibly complex the language is, particularly with the nuances between methods that seem to do the same thing. 

### "Toto, I've a feeling we're not in Bootcamp Prep anymore".

Call, apply and bind are all JavaScript methods that allow the programmer to change the value of the `this` keyword as it is applicable to a given function. 

## Function.prototype.call()
Call invokes the function and allows the programmer to pass in arguments one at a time. Arguments passed in are separated by commas (C for Call).

`
var person1 = {firstName: 'Samantha', lastname: 'Garcia'};
  var person2 ={firstName: 'John', lastname: 'Smith'};
     function say(greeting) {
		 
		console.log(greeting + ' ' + this.firstName + ' ' + this.lastName);
		}
		
		 say.call(person1, 'Hello'); // Hello Samantha Garcia
		 say.call(person2, 'Hello'); // Hello John Smith`

## Function.prototype.apply()
Apply invokes the function and allows the programmer to pass in arguments as an array. Apply is applicable to arrays (A for Array).

`
var person1 = {firstName: 'Samantha', lastname: 'Garcia'};
  var person2 ={firstName: 'John', lastname: 'Smith'};
     function say(greeting) {
		 
		console.log(greeting + ' ' + this.firstName + ' ' + this.lastName);
		}
		
		 say.apply(person1, ['Hello']);  // Hello Samantha Garcia
		 say.apply(person2, ['Hello']);  // Hello John Smith`

## Function.prototype.bind()
Bind returns a new function, allowing the programmer to pass in a `this` array and any number of arguments. Bind can be used to curry functions, also known as partial function application, which allows the use of a function (that accepts one or more arguments) to return a new function with some of the arguments already set. The function that is returned has access to the stored arguments and variables of the outer function. With bind, one can explicitly set the `this` value for invoking methods on objects. Methods can be borrowed and copied, and assigned to the variable to be executed as functions.

```
var person1 = {firstName: 'Samantha', lastname: 'Garcia'};
  var person2 ={firstName: 'John', lastname: 'Smith'};
     function say() {
		 
		console.log('Hello' + ' ' + this.firstName + ' ' + this.lastName);
		}
		
		 var sayHelloSamantha = say.bind(person1);
		 var sayHelloJohn = say.bind(person2);
		 
		 sayHelloSamantha();  // Hello Samantha Garcia
		 sayHelloJohn();  // Hello John Smith```
