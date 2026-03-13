# Reverse of a number

## Problem Statement

Write a program to generate the reverse of a given number N. Print the
corresponding reverse number.

Note : If a number has trailing zeros, then its reverse will not include them.
For e.g., reverse of 10400 will be 401 instead of 00401.

## Detailed Explanation

### Input format

Integer N

### Output format

Corresponding reverse number

### Constraints

$0 <= N < 10^8$

```md
Sample Input 1:
1234
Sample Output 1:
4321
Sample Input 2:
1980
Sample Output 2:
891
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
    int reverse = 0;
    while(n > 0)
    {
        reverse = (n % 10) + reverse * 10;
        n /= 10;
    }
    System.out.print(reverse);
}
}
```
