# Async / Await  
Async await is the syntax for asynchronous code which is built on top of promises .  
An async function always returns a promise object .  
**Await** keyword pauses execution of async code untill the promise resolves without blocking the main thread .   

```
async function getUser() {
    const users = await fetch('/api/user');
    const data = await users.json();
    return data;
}
```

## Error handling 
we can wrap an await call in try and catch block for error handling , resolved state is handled in try block and rejected state is handled in catch block.

```
async function getData() {
  try {
    const res = await fetch("/api/data");
    if (!res.ok) throw new Error("Request failed");
    return await res.json();
  } catch (err) {
    console.error(err.message);
  }
}
```

## Sequential vs Parallel 

Sequential is slower if independent that is if there are two tasks which does not depend on each other's output then calling them sequentially will be slower it is better to call them parallely .

```
async function sequential() {
  const a = await taskA();
  const b = await taskB();
  return [a, b];
}

```

```
async function parallel() {
  const [a, b] = await Promise.all([
    taskA(),
    taskB()
  ]);
  return [a, b];
}
  
```
**Dont** use For each loop they dont await   
for sequential we can use For of loop and for parallel we can use promise.all

```
for (const item of items) {
  await process(item);
}

await Promise.all(
  items.map(item => process(item))
);

```