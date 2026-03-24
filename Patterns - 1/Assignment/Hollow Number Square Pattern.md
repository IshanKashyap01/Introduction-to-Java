# Hollow Number Square Pattern

## Problem Statement

Print the following pattern for the given N number of rows.

**Pattern for N = 3**  

```ltf
123
1 2
123
```

## Detailed Explanation

### Input Format

Integer N (Total no. of rows)

### Output Format

Pattern in N lines

### Constraints

$0 <= N <= 50$

```ltf
Sample Input 1:
5
Sample Output 1:
12345
1   2
1   2
1   2
12345
Sample Input 2:
4
Sample Output 2:
1234
1  2
1  2
1234
```

## Solution

```java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        // write your code here !!
        Scanner sc = new Scanner(System.in);
        byte rows = sc.nextByte();
        for(byte row = 1; row <= rows; row++)
        {
            if(row != 1 && row != rows)
            {
                System.out.print(1);
                for(byte spaces = 0; spaces < rows - 2; spaces++)
                {
                    System.out.print(' ');
                }
                System.out.print(2);
            }
            else
            {
                for(byte column = 1; column <= rows; column++)
                {
                    System.out.print(column);
                }
            }
            System.out.println();
        }
    }
}
```
