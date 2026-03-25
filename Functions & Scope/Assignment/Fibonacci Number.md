# Fibonacci Number

## Problem Statement

Create a function that determines whether a given number N belongs to the
Fibonacci sequence. If N is found in the Fibonacci sequence, the function
should return true; otherwise, it should return false.

## Detailed Explanation

### Input Format

Integer N

### Output Format

true or false

### Constraints

$0 <= n <= 10^4$

```ltf
Sample Input 1:
5
Sample Output 1:
true
Explanation:
Fibonacci sequence begins 0, 1, 1, 2, 3, 5, ... and so on. Since 5 appears in the sequence.
Sample Input 2:
14
Sample Output 2:
false
```

## Solution

```Java
public class Solution 
{
    public static boolean checkMember(int n)
    {
        int prev = 0, next = 1, temp;
        while(prev <= n)
        {
            if(n == prev || n == next)
            {
                return true;
            }
            temp = next;
            next = next + prev;
            prev = temp;
        }
        return false;
    }
}
```
