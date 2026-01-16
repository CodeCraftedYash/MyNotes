# Global Execution Context
    global execution context is an execution environment created when the js script runs and it contains global vairabhles and functions . It is always present during program execution.  

# Function Execution Context
    function execution context is an execution environment for functions , it is created when a function is called and it contains its own isolated variables and functions.  

# Phases :
### each execution context goes through two distinct phases
- Memory Creation Phase : in this phase the js engine allocates memory for variables and functions.  
var is hoisted and initiallized with undefined , const and let are hoisted but not initiallized,  
they are placed in temporal dead zone (TDZ) until their declaration is reached  and functions are  
stored in full.

- Execution Phase : in this phase the code is executed line by line , variables are assigned their actual  
values and function bodies are run.

# Stack overflow :
when a function is called infinitely or when a recursion function is called without a proper base class, it causes the stack to exceed it maximum capacity causing stack overflow.