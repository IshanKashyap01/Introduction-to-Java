# Triangle Number Pattern

## Problem Statement

Print the following pattern for the given N number of rows.  
**Pattern for N = 3**  
1  
22  
333

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
1
22
333
4444
55555
Sample Input 2:
4
Sample Output 2:
1
22
333
4444
```

## Solution

```Java
import java.util.*;

public class Solution
{
    public static void main(String[] args)
    {
        // write your code !!!
        Scanner sc = new Scanner(System.in);
        byte rows = sc.nextByte();
        for(byte row = 1; row <= rows; row++)
        {
            for(byte column = 1; column <= row; column++)
            {
                System.out.print(row);
            }
            System.out.println();
        }
    }
}
```
