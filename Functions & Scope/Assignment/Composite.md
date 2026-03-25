# Composite

## Problem Statement

Your task is to write a function named print_composite that prints if there are
any composite numbers up to a given number, n.

Composite numbers are positive integers greater than 1 that have more than two
positive divisors. In other words, a composite number has factors other than 1
and itself.

## Detailed Explanation

### Output Format

The function should print all the composite numbers up to n if numbers are found within the range from 2 to n (inclusive).

```ltf
Sample Input 1:
10
Sample Output 1:
4
6
8
9
10
Explanation :
A composite number is a positive integer greater than 1 that has more than two positive divisors. In other words, it is not a prime number. Here are the composite numbers between 2 and 10:
4, 6, 8, 9, and 10
```

## Solution

```java
public class Solution
{
    public static void print_composite(int n)
    {
        // write your code logic here
        for(int i = 4; i <= n; i++)
        {
            if(isComposite(i))
            {
                System.out.println(i);
            }
        }
    }

    public static boolean isComposite(int n)
    {
        for(int i = 2; i <= n / 2; i++)
        {
            if(n % i == 0)
            {
                return true;
            }
        }
        return false;
    }
}
```
