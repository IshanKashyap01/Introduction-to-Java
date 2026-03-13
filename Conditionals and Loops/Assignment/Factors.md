# Factors

## Problem Statement

Write a program that takes a number as input and prints all its factors except
1 and the number itself.. If the number has only two factors (1 and the number
itself), then the program should print -1.

## Detailed Explanation

### Input Format

A single integer, n

### Output Format

All the factors of n excluding 1 and the number itself

### Constraints

$0 <= n <= 10,000$

```md
Sample Input 1:
8
Sample Output 1:
2 4

Explanation of Sample Output 1:
The factors for the number excluding 1 and itself are 2 and 4, so the output is 2 4.

Sample Input 2:
11
Sample Output 2:
-1

Explanation of Sample Output 2:
11 is a prime number having factors 1 and 11 so that output will be -1.
```

## Solution

```java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        // Write your code here
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        // assume that the number has no factors
        boolean hasFactors = false;
        // For each number from 2 to the half of n, check if it is a factor
        for(int i = 2; i <= n / 2; i++)
        {
            // Check if the i is a factor of n
            if(n % i == 0)
            {
                System.out.print(i + " ");
                hasFactors = true;
            }
        }
        if(!hasFactors)
        {
            System.out.println(-1);
        }
    }
}
```
