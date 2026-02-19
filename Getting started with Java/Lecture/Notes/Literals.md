# Literals

- Any constant value that can be assigned to a variable is called a literal in
Java

- These include but are not limited to characters, strings, boolean and decimal
numbers

- Numeric literals in Java have a default type:

    1. Integer literals: `int`

    2. Decimal literals: `double`

```java
float temperature = 23.22f;
```

- To store a `float` literal value, `f` is suffixed to the number

```java
long population = 3_000_000L;
```

- Whereas to store a `long` literal value, `L` is suffixed to the number

- Big numbers can be broken up by adding `_` instead of a `,`

```java
byte mask = 0b101;
short unixPermissions = 0755;
int color = 0xFF_00_FF;
```

- You can also store *binary*, *octal* and *hexadecimal* values in Java by
using prefixes `0b`, `0` and `0x` respectively

```java
// Avogadro's number is 6.022 x 10^23
double avogadro_sNumber = 6.022e23;
```

- For massive floating point values, `e` can be used for powers of $10$

```java
// ASCII for 65 is A
char option = 65;
```

- `char` will read numbers as ASCII values

```java
String phi = "The capital letter phi in Greek is written as: \u03c6";
```

- Unicode values can also be used by prefixing `\u` before the unicode value

- Boolean variables can only accept two values: `true` and `false`
