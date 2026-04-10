# Introduction to Strings

- `String` class uses a character array internally to store string values

- Strings in Java are immutable, therefore, a new String value is created every
time we update its value

- We can create a new string in the following ways:

```java
char[] charArr = {'a', 'b', 'c', 'd'};
byte[] byteArr = {97, 98, 99, 100};

// Passing a string literal
String literal = "This is a string";
// Passing a character array (value: abcd)
String charString = new String(charArr);
// Passing a byte array (value: abcd)
String byteString = new String(byteArr);
```

**Note**:

Character arrays behave differently when printed as is

```java
// Prints [I@<memory location>
System.out.println(byteArr);
// Prints abcd
System.out.println(charArr);
```
