# Diamond of Stars

## Problem Statement

Print the following pattern for the given number of rows.  
**Note: N is always odd.**

**Pattern for N = 5**  

```ltf
  *
 ***
*****
 ***
  *
```

## Detailed Explanation

### Input format

N (Total no. of rows and can only be odd)

### Output format

Pattern in N lines

### Constraints

$1 <= N <= 49$

```ltf
Sample Input 1:
5
Sample Output 1:
  *
 ***
*****
 ***
  *
Sample Input 2:
3
Sample Output 2:
  *
 ***
  *
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
        for(byte row = 1; row <= rows; row += 2)
        {
            // number of spaces = (rows - row) / 2
            for(byte spaces = 0; spaces < (rows - row) / 2; spaces++)
            {
                System.out.print(' ');
            }
            for(byte column = 0; column < row; column++)
            {
                System.out.print('*');
            }
            System.out.println();
        }
        for(byte row = (byte) (rows - 2); row > 0; row -= 2)
        {
            for(byte spaces = 0; spaces < (rows - row) / 2; spaces++)
            {
                System.out.print(' ');
            }
            for(byte column = 0; column < row; column++)
            {
                System.out.print('*');
            }
            System.out.println();
        }
    }
}
```
