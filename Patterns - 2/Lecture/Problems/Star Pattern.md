# Star Pattern

## Problem Statement

Print the following pattern

Pattern for N = 4

```ltf
    *
   *** 
  *****
 *******
```

**Hint**: As taught in the video, you just have to modify the code so that
instead of printing numbers, it should output stars ('*').

## Detailed Explanation

### Input Format

N (Total no. of rows)

### Output Format

Pattern in N lines

### Constraints

$0 <= N <= 50$

```ltf
Sample Input 1:
3
Sample Output 1:
   *
  *** 
 *****
Sample Input 2:
4
Sample Output 2:
    *
   *** 
  *****
 *******
```

## Solution

```Java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        for(int i = 1; i <= n; i++)        
        {
            for(int s = 1; s <= n - i; s++)
            {
                System.out.print(" ");                
            }
            for(int j = 1; j <= i; j++)
            {
                System.out.print("*");
            }
            for(int d = i - 1; d >= 1; d--)
            {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```
