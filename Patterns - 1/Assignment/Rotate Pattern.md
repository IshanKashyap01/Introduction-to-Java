# Rotate Pattern

## Problem Statement

Print the following pattern for the given N number of rows.

**Note:**
print spaces between the numbers.  

**Pattern for N = 3**  
1 2 3  
2 3 1  
3 1 2  

## Detailed Explanation

### Input Format

Integer N (Total no. of rows)

### Output Format

Pattern in N lines

### Constraints

$0 <= N <= 50$

```md
Sample Input 1:
5
Sample Output 1:
1 2 3 4 5
2 3 4 5 1
3 4 5 1 2
4 5 1 2 3
5 1 2 3 4
Sample Input 2:
4
Sample Output 2:
1 2 3 4 
2 3 4 1
3 4 1 2 
4 1 2 3
```

## Solution

```java
import java .util.Scanner;

public class Solution 
{
    public static void main(String args[]) 
    {
        // write your code logic !!
        Scanner sc = new Scanner(System.in);
        byte rows = sc.nextByte();
        for(byte row = 0; row < rows; row++)
        {
            for(byte column = 0; column < rows; column++)
            {
                // (row + column) % rows will keep rotating the value within the range 0 to rows - 1.
                //  By adding 1, the range becomes 1 to rows.
                System.out.print((row + column) % rows + 1 + " ");
            }
            System.out.println();
        }
    }
}

```
