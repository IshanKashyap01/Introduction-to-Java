# Filled K Shape

## Problem Statement

Print the following pattern for the given N number of rows.  
**Pattern for N = 4**  
4 3 2 1  
3 2 1  
2 1  
1  
2 1  
3 2 1  
4 3 2 1

## Detailed Explanation

### Input format

Integer N (Total no. of rows)

### Output format

Pattern in N lines

### Constraints

$0 <= N <= 50$

```ltf
Sample Input 1:
1
Sample Output 1:
1
Sample Input 1:
3
Sample Output 1:
3 2 1
2 1
1
2 1
3 2 1
```

## Solution

```java
import java.util.Scanner;
public class Solution 
{
    public static void main(String[] args) 
    {       
        /* Your class should be named Solution.
        * Read input as specified in the question.
        * Print output as specified in the question.
        */
        Scanner sc = new Scanner(System.in);
        byte rows = sc.nextByte();
        for(byte row = rows; row > 0; row--)
        {
            for(byte column = row; column > 0; column--)
            {
                System.out.print(column + " ");
            }
            System.out.println();
        }
        for(byte row = 2; row <= rows; row++)
        {
            for(byte column = row; column > 0; column--)
            {
                System.out.print(column + " ");
            }
            System.out.println();
        }
    }
}
```
