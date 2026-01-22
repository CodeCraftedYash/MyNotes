# == vs ===

=== (strict equality) operator compares both value and type  
Eg:  
false === 0 it will be  false because false is boolean and 0 is integer

== (abstract equality) operator perform type coercion which automatically changes type and then compares the operands  
false == 0 is true , false will be converted to 0 and then compared to 0   

falsy values  
```
false
0
-0
0n
""
null
undefined
NaN
```
 everything beside this are truthy

   
null is only equal to undefined
```
null == undefined //true
```
NaN is not equal to anything not even to itself
```
NaN == NaN //false
```