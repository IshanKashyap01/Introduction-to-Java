# Hourglass Pattern

## Problem Statement

You are given an integer N and you have to print the following pattern.

For N = 5:

```ltf
1 2 3 4 5
 2 3 4 5
  3 4 5
   4 5
    5
   4 5
  3 4 5
 2 3 4 5
1 2 3 4 5
```

For N = 6:

```ltf
1 2 3 4 5 6
 2 3 4 5 6
  3 4 5 6
   4 5 6
    5 6
     6
    5 6
   4 5 6
  3 4 5 6
 2 3 4 5 6
1 2 3 4 5 6
```

## Detailed Explanation

### Input Format

The first and only line of input contains an integer, that denotes the value of N.

### Output Format

Print the pattern, as described in the problem statement.

### Constraints

$1 <= N <= 50$

Time Limit: 1 second

## Solution

```java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        byte rows = sc.nextByte();
        for(byte row = 1; row <= rows; row++)
        {
            //  There are row - 1 spaces
            for(byte spaces = 0; spaces < row - 1; spaces++)
            {
                System.out.print(' ');
            }
            // The line starts from row to rows
            for(byte column = row; column <= rows; column++)
            {
                System.out.print(column + " ");
            }
            System.out.println();
        }
        // Reverse of the above pattern starting from rows - 1
        for(byte row = (byte) (rows - 1); row > 0; row--)
        {
            for(byte spaces = 0; spaces < row - 1; spaces++)
            {
                System.out.print(' ');
            }
            for(byte column = row; column <= rows; column++)
            {
                System.out.print(column + " ");
            }
            System.out.println();
        }
    }
}
```
