# Modules
Modules allow you to split code into reusable files.
## import / export
```
// math.js (exporting)
export const add = (a, b) => a + b;
export const sub = (a, b) => a - b;

// single export
export function multiply(a, b) {
  return a * b;
}

//importing

import { add, sub } from "./math.js";

add(2, 3);

```
---

## Named vs Default exports  
 
 ### Named Imports  
- Multiple exports per file
- Must use same names while importing
- Curly braces required
```
import { formatDate, parseDate } from "./utils.js";

```
### Default Imports
- Only one default export per file
- Can be imported with any name
- No curly braces
---

## Mixing Named + Default

```
// api.js
export default function fetchData() {}
export const BASE_URL = "https://api.example.com";

//import
import fetchData, { BASE_URL } from "./api.js";

```
---

## Module scope

importing varibales throws reference error , since variables are not global scoped 

---

## Tree shaking concept
Tree shaking is a build-time optimization that removes unused exports from final bundles. It works only with ES modules that is import export and not require
```
// math.js
export const add = () => {};
export const sub = () => {};
export const mul = () => {};

// app.js
import { add } from "./math.js";

```

sub and mul are removed since they are unused , in bundle.  
benfits : 
- Smaller bundle size
- Faster load time
- Better performance