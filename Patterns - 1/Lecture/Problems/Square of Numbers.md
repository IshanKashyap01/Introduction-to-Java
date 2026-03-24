# Square of Numbers

## Problem Statement

Print the following pattern for the given N number of rows.  
**Pattern for N = 3**  
321  
321  
321

## Detailed Explanation

### Input Format

Integer N (Total no. of rows)

### Output Format

Pattern in N lines

### Constraints

$0 <= N <= 50$

```md
Sample Input1:
5
Sample Output 1:
54321
54321
54321
54321
54321
Sample Input 2:
4
Sample Output 2:
4321
4321
4321
4321
```

## Solution

```java
import java.util.Scanner;

public class Solution
{
    public static void main(String[] args) 
    {
        // write your code !!
        Scanner sc = new Scanner(System.in);
        byte side = sc.nextByte();
        for(byte row = 0; row < side; row++)
        {
            for(byte column = side; column > 0; column--)
            {
                System.out.print(column);
            }
            System.out.println();
        }
    }   
}
```
