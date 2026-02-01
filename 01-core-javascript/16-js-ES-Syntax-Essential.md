# ES6 Essentials 

## let and const  
### let
- Block-scoped (limited to {}).  
- Can be reassigned.  
- Preferred over var.

### const

- Block-scoped.  
- Cannot be reassigned.  
- For objects/arrays, reference is constant, not the content. 

---

## Arrow Functions
lexically bind this (no own this)  
```
const greet = (name) => {
  return `Hello ${name}`;
};
```

---

## Template literal
Supports interpolation
```
const name = "Yash";
const msg = `Hello ${name}, welcome!`;
```

---  

## Destructuring  
 ## object destructuring
 extracting out inner elements
 ```
const user = { name: "Yash", age: 20 };

const { name, age } = user;
 ```
 ## array destructuring

 ```
 const arr = [10, 20, 30];

const [a, b] = arr;
```
---

## Spread (...) and Rest (...) Operators

### Spread
Used to expand elements
```
//array
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4];

//object
const user = { name: "Yash" };
const updatedUser = { ...user, age: 20 };

```

### Rest Operator
Used to collect remaining elements.
```
const sum = (...numbers) => {
  return numbers.reduce((a, b) => a + b, 0);
};

const [first, ...rest] = [1, 2, 3, 4];
```
---

## Default Parameters  
Assign default values to function parameters.
```
const greet = (name = "Guest") => {
  return `Hello ${name}`;
};
```