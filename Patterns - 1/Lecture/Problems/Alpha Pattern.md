# Alpha Pattern

## Problem Statement

Print the following pattern for the given N number of rows.

**Pattern for N = 3**  
AAA  
BBB  
CCC

## Detailed Explanation

### Input Format

Integer N (Total no. of rows)

### Output Format

Pattern in N lines

### Constraints

$10 <= N <= 50$

```ltf
Sample Input 1:
4
Sample Output 1:
AAAA
BBBB
CCCC
DDDD
Sample Input 2:
5  
Sample Output 2:
AAAAA
BBBBB
CCCCC
DDDDD
EEEEE
```

## Solution

```Java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        // write your code logic here !!
        Scanner sc = new Scanner(System.in);
        byte rows = sc.nextByte();
        for(byte row = 0; row < rows; row++)
        {
            for(byte column = 0; column < rows; column++)
            {
                System.out.print((char) ('A' + row));
            }
            System.out.println();
        }
    }
}
```
