# Reverse Char Pattern

## Problem Statement

Print the following pattern for the given N number of rows.

**Pattern for N = 5**  
E  
ED  
EDC  
EDCB  
EDCBA

## Detailed Explanation

### Input format

Integer N (Total no. of rows)

### Output format

Pattern in N lines

### Constraints

$0 <= N <= 50$

```ltf
Sample Input 1:
7

Sample Output 1:
G
GF
GFE
GFED
GFEDC
GFEDCB
GFEDCBA
Sample Input 1:
6
Sample Output 1:
F
FE
FED
FEDC
FEDCB
FEDCBA
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
                System.out.print((char) ('A' + rows - 1 - column));
            }
            System.out.println();
        }
    }
}
```
