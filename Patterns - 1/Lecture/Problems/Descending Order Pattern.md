# Descending Order Pattern

## Problem Statement

Print the following pattern for the given N number of rows.  
**Note: Print spaces between the numbers. Pattern for N = 5**  
5  
5 4  
5 4 3  
5 4 3 2  
5 4 3 2 1

## Detailed Explanation

### Input format

Integer N (Total no. of rows)

### Output format

Pattern in N lines

### Constraints

$0 <= N <= 50

```md
Sample Input 1:
7
Sample Output 1:
7
7 6
7 6 5 
7 6 5 4 
7 6 5 4 3 
7 6 5 4 3 2 
7 6 5 4 3 2 1
Sample Input 2:
6
Sample Output 2:
6
6 5 
6 5 4 
6 5 4 3 
6 5 4 3 2 
6 5 4 3 2 1
```

## Solution

```java
import java.util.*;

public class Solution
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        byte rows = sc.nextByte();
        for(byte row = 1; row <= rows; row++)
        {
            for(byte column = 0; column < row; column++)
            {
                System.out.print(rows - column + " ");
            }
            System.out.println();
        }
    }
}
```
