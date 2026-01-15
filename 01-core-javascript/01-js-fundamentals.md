# Engine Overview

Javascript engine is a software component that parses and interprets high level javascript code  
into low level machine code. 
Modern engines use JIT (just in time) compilation , it has optimized performance


---


# How JS Run in browser

The browser first downloads the javascript code then then the javascript engine parses that  
javascript code and divides it into a structured format called AST (abstract syntax tree).  
Then the engine compiles the code into machine code using JIT comilation (just in time).  
Then the Javascript code is executed inside an **execution context**.


---
  

# Single threaded nature

Single thread in js mean it has a single call stack and it executes the code line by line one at a time.  
This avoids issues such as race conditions and shared memory conflicts.

---


# Synchronous vs Asynchronous exection

Synchronous nature means sequential that is the code runs in a single line one after another.  
The other block runs after the first block has finished.  
It has some issues like code blocking if the previous code is too long the next code could posibly run before the first one finishes.  
Asynchronous nature means concurrent or non blocking . It does not block the code it runs the functions declared as async after the main stack has finished all the functions within it .   

## note
- Concurrency means multiple tasks are in progress at the same time, but not necessarily executing at the same instant  
- A race condition occurs when the final result depends on the order in which concurrent operations complete, and that order is unpredictable.  
  Why It’s Dangerous
    - Bugs appear randomly
    - Hard to reproduce
    - Depends on timing
- A shared memory conflict happens when multiple threads access and modify the same memory location at the same time without coordination.