# Data Type 

## primitive :  
   primitive data types are stored by value, immutable, and stored in Stack Memory  
eg : number, string, null, undefined, boolean, symbol, bigint.  

## non-primitive :  
  non primitive data types are stored by reference , mutable and stored in heap memory .  
eg : object, array, functions .  

### pass by value  
```
function update (x) {
    x = 20;
}
let a = 10; 
update(a);

==> a = 10
```
*a* did not changed because x recieves a copy of a not the actual variable *a*  
### pass by reference  
```
const object = { x : 5 };

```

```
typeof 10           // "number"  
typeof "a"          // "string"  
typeof true         // "boolean"  
typeof undefined    // "undefined"  
typeof Symbol()     // "symbol"  
typeof 10n          // "bigint"  
typeof function(){} // "function" 
typeof null // "object" (legacy bug)
```

when object is created its reference is stored in Stack but the data within it is stored in heap .  
It is because stack needs fixed size , its really fast and it gets cleaned up automatically  
Whereas object can shrink and grow, can be shared across scope and can live beyond one function call Therefore object can not live in stack ; they live in heap .