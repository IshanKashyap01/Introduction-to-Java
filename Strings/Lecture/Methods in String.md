# Commonly Used Functions for Strings

```java
// Returns "string"
String substring = literal.substring(10);
// Returns "is"
substring = literal.substring(5, 7);
// Returns "Th@s @s a str@ng"
String str = literal.replace('i', '@');
```

- `length()` returns the length of the string

- `trim()` removes blank spaces from both ends and returns the string

- `substring()` returns a subset of the string, where end index is optional and
excluded

- `replace()` replaces all the appearances of a target character with the given
character

```java
if(literal.indexOf("is") == literal.lastIndexOf("is"))
{
    // will search for the first appearance of '@' starting from index 4
    System.out.print(str.indexOf('@', 4));
}
// will return 0 
System.out.println(charString.compareTo(byteString));
```

- `indexOf()` returns the index of the *first* appearance of the given
substring in the string; returns `-1` if not found

- `lastIndexOf()` returns the index of the *last* appearance of the given
substring in the string; returns `-1` if not found

- `equals()` checks if each character in two strings are the same or not

- `compareTo()` if the two strings are of different length:

    1. It returns the difference of their length

    2. Else, it compares and returns the difference in the unicode value of
    each character
