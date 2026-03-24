# Inverted Number Pattern

## Problem Statement

Print the following pattern for the given N number of rows.  
**Pattern for N = 4**  
4444  
333  
22  
1

## Detailed Explanation

### Input format

Integer N (Total no. of rows)

### Output format

Pattern in N lines

### Constraints

$0 <= N <= 50$

```ltf
Sample Input 1:
5
Sample Output 1:
55555 
4444
333
22
1
Sample Input 2:
6
Sample Output 2:
666666
55555 
4444
333
22
1
```

## Solution

```Java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        byte rows = sc.nextByte();
        for(byte row = rows; row > 0; row--)
        {
            for(byte column = 0; column < row; column++)
            {
                System.out.print(row);
            }
            System.out.println();
        }
    }
}
```
