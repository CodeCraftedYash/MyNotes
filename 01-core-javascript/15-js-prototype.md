# Prototype

prototype is an internal mechanism of javascript that allows multiple objects to share behaviour without duplicating methods.  
for example if there are 1000 objects and they all need to call a method greet() , we will have 1000 duplicates of this greet() method , so we use prototype to store this greet method and share with the 1000 objects.  
## _ proto _ 
__proto __ is an internal reference present on every JavaScript object.
It points to the object’s prototype and is used for property and method lookup.
```
u.__proto__ === User.prototype // true
```

## Prototype Chain

When a property is accessed on an object, JavaScript:

- Looks for it on the object itself
- If not found, looks on its prototype
- Continues until Object.prototype
- Stops at null

## InstanceOf  
The instanceof operator checks whether a constructor’s prototype exists in an object’s prototype chain.