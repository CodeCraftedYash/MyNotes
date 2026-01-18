# Hoisting mechanism  
hoisting mechanism is js behaviour , in which before code execution, variables and functions are allocated memory.  
var is initialized with undefined and let and const are hoisted but not initialized they are put in TDZ and functions  
are hosited fully.  
   
     
      
# var vs let vs const  
| Feature | var | let | const |
|--------|-----|-----|-------|
| Scope | Function | Block | Block |
| Hoisting | Yes (undefined) | Yes (TDZ) | Yes (TDZ) |
| Re-declaration | Allowed | ❌ | ❌ |
| Re-assignment | Allowed | Allowed | ❌ |

# temporal dead zone  
Temporal Dead Zone is the time between memory allocation and execution phase or when the variable come into scope and it   
initialization that happens in execution phase.  

# function declaration vs function expression 
 function declaration is just normal function and function expression is when we store that function into a var.  
 function declaration are fully hoisted , but function expression behaves like a variable and is subjected to TDZ.  
 Both of these can be accessed before declaration.  