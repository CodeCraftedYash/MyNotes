# Promises
Promises are objects that represents eventful completion of asynchronous operation its result .  
There are three states of a Promise : Pending , fulfilled and Rejected . 

**.then** : handles fulfiled state   
**.catch** : handles rejected state   
**.finally** : handles the state irresepctive of fulfilled or rejected 

## Promise Chaining    
promise chaining means each .then can return a new promise and we can place .then as many times we want , if any of these then fails with error we can catch it in a single .catch . We dont need multiple .catch 

## Throwing vs Rejecting   
they are both the same  
```
throw new Error("error");      // rejects promise
return Promise.reject("err"); // same effect

```

## Promise combinators  
promise combimators are static methods that take an array of promises and manage them all at once  
promise.all : resolves when all promises resolve and rejects if any one throws error .  
promise.allSettled  : resolves when all promises settle , never rejects .   
promise.race  :  as soon as the first promise settles , can resolve or reject .  
promise.any  :  resolves when first promise fulfills, ignores rejection . 