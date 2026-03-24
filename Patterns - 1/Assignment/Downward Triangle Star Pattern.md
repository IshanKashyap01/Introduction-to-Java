# Downward Triangle Star Pattern

## Problem Statement

Print the following pattern for the given N number of rows.

**Pattern for N = 3**  

```md
***  
 **  
  * 
```

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
*****
 ****
  ***
   **
    *
Sample Input 2:
4
Sample Output 2:
 ****
  ***
   **
    *
```

## Solution

```java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        // write the logic here !!
        Scanner sc = new Scanner(System.in);
        byte rows = sc.nextByte();
        for(byte row = rows; row > 0; row--)
        {
            for(byte spaces = 0; spaces < rows - row; spaces++)
            {
                System.out.print(" ");
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
