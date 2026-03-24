# Pyramid of Numbers

## Problem Statement

Print the following pattern for the given N number of rows.  
**Note:**  
After printing the number, please ensure to add a space; otherwise, some test cases may fail.

**Pattern for N = 4**  

```md
   1
  2 2
 3 3 3
4 4 4 4
```

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
   2 2
  3 3 3
 4 4 4 4
5 5 5 5 5
```

## Solution

```java
import java.util.Scanner;

public class Solution
{  
    public static void main(String ar[])  
    {  
        // write your code logic here !!!
        Scanner sc = new Scanner(System.in);
        byte rows = sc.nextByte();
        for(byte row = 1; row <= rows; row++)
        {
            System.out.print("\t");
            for(byte spaces = 0; spaces < rows - row; spaces++)
            {
                System.out.print(" ");
            }
            for(byte column = 1; column <= row; column++)
            {
                System.out.print(row + " ");
            }
            System.out.println();
        }
    }  
}
```
