# Triangle of Numbers

## Problem Statement

Print the following pattern for the given number of rows.  
**Pattern for N = 4**

```ltf
   1
  232
 34543
4567654
```

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
           1
          232
         34543
        4567654
       567898765
Sample Input 2:
4
Sample Output 2:
           1
          232
         34543
        4567654
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
        for(byte row = 1; row <= rows; row++)
        {
            for(byte spaces = 0; spaces < rows - row; spaces++)
            {
                System.out.print(' ');
            }
            int column;
            for(column = row; column <= 2 * row - 1; column++)
            {
                System.out.print(column);
            }
            // -2 because the last loop adds an extra 1 to column before ending
            for(column -= 2; column > row - 1; column--)
            {
                System.out.print(column);
            }
            System.out.println();
        }
    }
}

```

### Explanation

Divide the pattern into *spaces*, *increasing* and *decreasing numbers*

For each row `i` (starting from `1` to `n`):

1. There are `n - i` spaces

2. First, the column `j` starts at `i` and stops at `2i - 1`

3. Then the column restarts from `j - 1` and ends at `i - 1`
