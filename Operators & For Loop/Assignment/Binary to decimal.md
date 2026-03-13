# Binary to decimal

## Problem Statement

Given a binary number as an integer N, convert it into decimal and print.

## Detailed Explanation

### Input format

An integer N in the Binary Format

### Output format

Corresponding Decimal number (as integer)

### Constraints

$0 <= N <= 10^9$

```md
Sample Input 1:
1100
Sample Output 1:
12
Sample Input 2:
111
Sample Output 2:
7
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
        int binaryNumber = sc.nextInt();
        int decimalNumber = 0;
        int currentDigit, digitCount = 0;
        while(binaryNumber > 0)
        {
            currentDigit = binaryNumber % 10;
            if(currentDigit == 1)
            {
                decimalNumber += Math.pow(2, digitCount);
            }
            digitCount++;
            binaryNumber = binaryNumber / 10;
        }
        System.out.println(decimalNumber);
    }
}
```
