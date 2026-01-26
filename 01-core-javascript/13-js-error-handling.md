 # Error handling

 error can be caught using two ways either in catch block of promise or try-catch or by throwing an error manually .  

 ## custom errors

 we can create custom error class by extending the error class provided by javascript 

 ```
 class ValidationError extends Error {
  constructor(message) {
    super(message);
    this.name = "ValidationError";
  }
}
 ```
 ## error propagation
 If an error is not handled, it bubbles up the call stack
 ```
 function levelOne() {
  levelTwo();
}

function levelTwo() {
  throw new Error("Something went wrong");
}

levelOne(); // Error propagates upward

 ```
 ## Global error handling
Used to catch unhandled errors that escape local handlers.
 ```
 window.onerror = function (message, source, lineno, colno, error) {
  console.error("Global error:", message);
};

window.addEventListener("unhandledrejection", event => {
  console.error("Unhandled Promise rejection:", event.reason);
});

 ```