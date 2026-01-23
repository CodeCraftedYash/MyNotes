# Event loop  
Event loop is the mechanism that allows the javascript to handle asynchronous operations by controlling the order of execution of code.   
Javascript first executes all the synchronous code present in the call stack , once the stack is empty Javascript drains the microtask queue . After all microtask queue is executed , the event loop executes one task from the macrotask queue and then repeats this cycle .  
Call stack consits of  all the synchronous functions call, variables initialization , loops and conditional statements .    
micro task queue consists of promised - based callbacks such as then , catch , finally and async/await .   
macro task queue consists of timers and events based callbacks , such as setTimeout , setTimeInterval and DOM event handlers .  