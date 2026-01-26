# Objects  
objects are non primitive data type, their reference is stored in the stack memory and the object is stored in the heap memory .   

## Objects creation pattern

    object literal
    ```
    const user = {
        name : "Yash"
    }
    ```

    constructor function  
    ```
    function User(name, age) {
    this.name = name;
    this.age = age;
    }

    const u1 = new User("A", 20);

    ```
    using class
    ```
    class User {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
    }

    ```
    factory function 
    ```
    function createUser(name, age) {
    return { name, age };
    }
    ```

    object.create  

    ```
    const proto = {
    greet() {
        console.log("Hi");
    }
    };

    const user = Object.create(proto);
    user.name = "Yash";

    ```
## Properties Description  
Every object property has meta data :   
- value  : The actual value stored
- writable  :  Can the value be changed
- enumerable : Does it appear in loops
- configurable  : 	Can it be deleted or redefined

```
const user = {};

Object.defineProperty(user, "id", {
  value: 101,
  writable: false,
  enumerable: true,
  configurable: false
});

```

## Object.freeze, seal, preventExtensions  
| Method                       | Add | Delete | Modify |
| ---------------------------- | --- | ------ | ------ |
| `Object.preventExtensions()` | ❌   | ✅      | ✅      |
| `Object.seal()`              | ❌   | ❌      | ✅      |
| `Object.freeze()`            | ❌   | ❌      | ❌      |


## Object.keys, values, entries
```
const user = { name: "Yash", age: 21 };

Object.keys(user);    // ["name", "age"]
Object.values(user); // ["Yash", 21]
Object.entries(user); // [["name", "Yash"], ["age", 21]]

Object.entries(user).forEach(([key, value]) => {
  console.log(key, value);
});

```