# GCD

## Problem Statement

Given two numbers, x, and y, calculate and Return their GCD.

GCD stands for "Greatest Common Divisor." It refers to the largest positive
integer that divides two or more numbers without leaving a remainder.

## Detailed Explanation

### Input format

x and y (separated by space)

### Output format

GCD of x and y

```ltf
Sample Input 1:
20 
5
Sample Output 1:
5
Sample Input 2:
96 
28
Sample Output 2:
4
Explanation :
One way to find the GCD is to use the prime factorization method:
Prime factorization of 96: 96 = 2*2*2*2*2*3
Prime factorization of 28: 28 = 2*2* 7
Common prime factors: 2*2
Therefore, the GCD of 96 and 28 is 4.
```

## Solution

```java
public class Solution 
{
    public static int findGCD(int a, int b) 
    {
        // Euclidean Algorithm
        int smaller = a < b ? a : b;
        int larger = a > b ? a : b;
        int remainder;
        while(smaller != 0)
        {
            remainder = larger % smaller;
            larger = smaller;
            smaller = remainder;
        }
        return larger;
    }
}
```

### Explanation

The algorithm used for calculating the GCD of two numbers is known as
*Euclidean Algorithm*. Following are its steps:

1. Start with two integers `a` and `b` where `a` is greater than `b`

2. Repeat the following until `b` becomes `0`:

    I. Calculate the remainder of `a` divided by `b` (`a % b`)

    II. Update `a` with the value of `b`

    III. Update `b` with the value of the remainder

3. Return `a` as the GCD
