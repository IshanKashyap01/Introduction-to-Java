# All Prime Numbers

## Problem Statement

Given an integer N, print all the prime numbers that lie in the range 2 to N
(both inclusive).

Print the prime numbers in different lines.

## Detailed Explanation

### Input Format

Integer N

### Output Format

Prime numbers in different lines

### Constraints

$1 <= N <= 100$

```md
Sample Input 1:
9
Sample Output 1:
2
3
5
7
Sample Input 2:
20
Sample Output 2:
2
3
5
7
11
13
17
19
```

## Solution

```java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        /* Your class should be named Solution.
        * Read input as specified in the question.
        * Print output as specified in the question.
        */
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        for(int i = 2; i <= n; i++)
        {
            boolean isPrime = true;
            for(int j = 2; j <= i / 2; j++)
            {
                if(i % j == 0)
                {
                    isPrime = false;
                    break;
                }
            }
            if(isPrime)
            {
                System.out.println(i);
            }
        }
    }
}
```
