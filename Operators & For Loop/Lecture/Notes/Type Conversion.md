# Type Conversion

- Smaller types are automatically converted to larger types (**widening**
**conversion**)

- However, larger types cannot be converted to smaller ones due to possible
loss of data (**narrowing conversion**)

```java
byte a = 10 + 20;
```

- Line 1 compiles as the compiler computes the value and sees that it fits a
`byte`

```java
byte a = 130;
float b = 23.48;
```

- Line 1 will not compile because `130` is larger than a byte

- Line 2 will not compile because `23.48` is a `double` value
