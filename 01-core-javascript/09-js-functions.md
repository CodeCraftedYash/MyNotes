# Functions 

there are different types of functions such as :  
- Function Declaration 
- Function Expression
- Arrow Function  
- Higher Order Function  
- Callback Function 
- IIFE ( Immedietly Invoked Function Expression )  

## Function Declaration  
```
function fn() {
    console.log("Function called");
}
```
function declaration are made using function keyword , they are hoisted fully  

## Function Expression  
```
const fn = function () { //function can be named or anonymous
    console.log("function called)
}
```
function expression are not hoisted, They behave like varibales and are put in TDZ during memory creation phase.

## Arrow Function  

```
const fn = () => {
    console.log("function called");
}
```
arrow function are same as function expression , just a change in their syntax  

## Higher Order Function  
```
function HOF(cb) {
    return cb(10);
}
```
Higher Order Function is a function that accept a function as parameter or return a function or both 

## Callback Function  
```
const handleClick = () => {
    console.log("clicked");
}

fn(handleClick);
```
a callback function is a function that is send to another function as argument and executed later .

## IIFE (Immediately Invoked Function Expression)  
 IIFE is a function that is executed immediately after creation 
 ```
 (function (){
    console.log('function invoked immediately');
 })();
 ```

