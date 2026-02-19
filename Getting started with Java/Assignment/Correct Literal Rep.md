# Correct Literal Representation

## Problem Statement

The values given below need to be assigned to the specified data types.
However, each value is incorrectly formatted for its intended data type.
Your task is to:

- Correct the representation of each value so it matches its specified data
type.

- Declare the variables using the correct data types. (The variable name could
be anything, like for ex: int value=26)

- Print each variable's value on a new line.

### Incorrect values provided

- `int: 26.0`
- `float: 3._1415`
- `double: 23.411f`
- `String: 'WritingCleanerCode'`

### Hint

- `int` should contain a whole number.

- `float` should contain a decimal number with f at the end.

- `double` should contain a decimal number without any suffix.

- `String` should be enclosed in double quotes.

## Solution

```java
public class DebugAndPrintLiterals
{
    public static void main(String[] args) 
    {
        //Declare and initialize the variables with proper literal representation
        int i = 26;
        float f = 3.1415f;
        double d = 23.411;
        String s = "WritingCleanerCode";
        //Print each literal value in new line.
        System.out.println(i);
        System.out.println(f);
        System.out.println(d);
        System.out.println(s);    
    }
}
```
