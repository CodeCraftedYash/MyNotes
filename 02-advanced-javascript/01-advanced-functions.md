# Advanced Functions

## First class Function  

In JavaScript, functions are first-class citizens, meaning they can be:

    Assigned to variables
    Passed as arguments
    Returned from other functions
    Stored in data structures (arrays/objects)  
this is the foundation for functional programming in javascript 

## Higher Order Function 

Higher order function is a function that either takes a function as argument , returns a function or both .  
It is built on top of first class function .  
They are used for  
- Code reusability
- Abstraction
- Cleaner, declarative code

## Callback function  
these functions are sent to another function as arguments to be executed later .  
Types 
- Synchronous callback : executed immediately
- Asynchronous callback : executed later 

## Callback Hell
Nested callbacks → hard to read and maintain
```
getUser(function(user) {
  getPosts(user.id, function(posts) {
    getComments(posts[0].id, function(comments) {
      console.log(comments);
    });
  });
});
```
Problems:
- Deep nesting
- Hard debugging
- Poor readability

## Error first callback pattern (node.js standard)
```
function fetchData(callback) {
  const error = null;
  const data = "Some data";

  callback(error, data);
}

fetchData((err, data) => {
  if (err) {
    console.error(err);
    return;
  }
  console.log(data);
});
```

## inversion of Control

When using callbacks, you give control to another function.
```
function doTask(callback) {
  callback();
}
```
Problem:

- You don’t control when/how callback is executed
- Can lead to bugs


## Modern Solution
Callbacks → Promises → Async/Await
```
// Promise version
fetchData()
  .then(data => console.log(data))
  .catch(err => console.error(err));

// Async/Await
async function run() {
  try {
    const data = await fetchData();
    console.log(data);
  } catch (err) {
    console.error(err);
  }
}
```