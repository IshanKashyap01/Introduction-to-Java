# Type Casting

```java
short year = 2030;
byte age = 39;
short birthYear = year - age;
```

- Line 3 will not compile and you'll get an error saying that you're converting
an `int` to a `short`

- This error can be fixed by *explicitly type casting* the `int` to `short`

```java
short birthYear = (short) (year - age);
```

- This converts the resulting value to a `short` data type thus fixing the
error

```java
char a = 'a';
// ab will be b
char b = (char) (a + 1); 
```

- `char` will automatically convert to `int` on addition operations but to do
the opposite, you need *explicit type casting*
