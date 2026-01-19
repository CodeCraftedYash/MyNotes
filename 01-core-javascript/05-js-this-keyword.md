# This keyword

This keyword refers to the object that is used to call a function, allowing the function to access the objects properties  
<code>
const user = {  
      name: "yash",  
      login: function print() {   
        console.log( this.name + " logged in " )  
    }
}
</code>

**name** is not a variable , It is a property of user object , so without this it will give reference error,  
 because name without this looks for variable not property

## global context : 
this keyword refers to window  

## strick mode : 
in strick mode this is undefined  


## object method :
in object method it refers to the object that called the function  

## arrow function : 
In arrow functions: this inherits from the enclosing lexical scope and does not change,  
even if called with call(), apply(), or bind().  

## constructor  :  
In constructors (with new): this refers to the newly created object

with call(), apply(), bind() this can be set to any object .  
<code> 
const greet = function() { console.log(`Hello, ${this.name}`); };  
const person1 = { name: 'Alice' };  
greet.call(person1); // Output: "Hello, Alice"</code>