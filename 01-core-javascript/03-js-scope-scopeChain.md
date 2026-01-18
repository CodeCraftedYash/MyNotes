# Scope  
#### scope determines where a variable is accessible in the program  



# Global Scope  
variables are declared outside a function and are accessible everywhere  

  

# Functional Scope  
variables are declared within a function and are accessible only within it   



# Block Scope  
variables are declared within a curly brackets {} using let or const and are accessible only within it  
var are function scoped   



# Lexical Scope  
it means scope is determined by where the function is written and not where it is called.    



# Scope Chain  

when variables is used Javascript first checks the current scope , then parent scope and then global scope. 
If the variable was not found in any of these It throws reference error