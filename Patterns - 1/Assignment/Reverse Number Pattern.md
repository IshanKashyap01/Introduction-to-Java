# Reverse Number Pattern

## Problem Statement

Print the following pattern for the given N number of rows.

**Pattern for N = 4**  
1  
21  
321  
4321  

## Detailed Explanation

### Input format

Integer N (Total no. of rows)

### Output format

Pattern in N lines

### Constraints

$0 <= N <= 50$

```md
Sample Input 1:
5
Sample Output 1:
1
21
321
4321
54321
Sample Input 2:
6
Sample Output 2:
1
21
321
4321
54321
654321
```

## Solution

```Java
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
        for(byte row = 1; row <= rows; row++)
        {
            for(byte column = row; column > 0; column--)
            {
                System.out.print(column);
            }
            System.out.println();
        }
    }
}
```
