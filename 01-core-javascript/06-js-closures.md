# Closures  
A closure is a function that retains access to variables from its lexical scope .  
It happens because the function carries a reference to its lexical scope  
Closures solve the problem of state persistence, data encapsulation, and controlled  
memory access without relying on global variables.
{ lexical scope :  accessibility of variables is determined by where the code is written  
in the source file, not by where a function is called}  
<code>
    function outer() {  
        let counter = 0;  
        function inner() {  
            return counter++ ;
        }
        return inner;
    }
    const fn = outer();
    fn();
</code>