# Interesting Alphabets

## Problem Statement

Print the following pattern for the given number of rows.  
**Pattern for N = 5**  
E  
DE  
CDE  
BCDE  
ABCDE

## Detailed Explanation

### Input format

N (Total no. of rows)

### Output format

Pattern in N lines

### Constraints

$0 <= N <= 26$

```ltf
Sample Input 1:
8
Sample Output 1:
H
GH
FGH
EFGH
DEFGH
CDEFGH
BCDEFGH
ABCDEFGH
Sample Input 2:
7
Sample Output 2:
G
FG
EFG
DEFG
CDEFG
BCDEFG
ABCDEFG
```

## Solution

```Java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        //Your code goes here
        Scanner sc = new Scanner(System.in);
        byte rows = sc.nextByte();
        for(byte row = 1; row <= rows; row++)
        {
            for(byte column = 0; column < row; column++)
            {
                System.out.print((char) ('A' + rows - row + column));
            }
            System.out.println();
        }
    }
}
```
