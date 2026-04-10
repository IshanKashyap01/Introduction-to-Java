# Memory Allocation of Strings

```java
// stored in the pool
String str = "This is a string";
// stored in the heap
String sub1 = str.substring(0);
// stored in the pool
String sub2 = str.substring(0).intern();
// will return true
boolean bool1 = str == sub2;
// will return false
boolean bool2 = str == sub1;
```

- `String` being an object data type is always stored in the heap

- However, some strings are stored in a special place in the heap known as the
**string/intern pool**

- The string pool is a space where duplicates are not created to optimize space

- Strings can either be created as literals, using the constructor (`String()`)
or as return values of functions like `substring()` or `trim()`

- Only literals are stored in the string pool while others are stored in the
heap like regular objects

- Although, they can be explicitly put in the pool by calling the `intern()`
function
