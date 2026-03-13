# Square Root (Integral)

## Problem Statement

Given a number N, find its square root. You need to find and print only the
integral part of square root of N.

For eg. if number given is 18, answer is 4.

## Detailed Explanation

### Input format

Integer N

### Output Format

Square root of N (integer part only)

### Constraints

$0 <= N <= 10^8$

```md
Sample Input 1:
10
Sample Output 1:
3
Sample Input 2:
4
Sample Output 2:
2
```

## Solution

```Java
import java.util.Scanner;

public class Main 
{
    public static void main(String[] args) 
    {
        // Write your code here
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int root = 0;
        for(int i = 1; i * i <= n; i++)
        {
            root = i;
            if(i * i == n)
            {
                break;
            }
        }
        System.out.println(root);
    }
}
```
