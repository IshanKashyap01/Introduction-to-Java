# Terms of AP

## Problem Statement

Write a program to print the first x terms of the mathematical series 3N + 2
which are not multiples of 4.

The series is defined as:

T(N) = 3N + 2, where N is a positive integer starting from 1. Your task is to
print the first x terms of this series, but you should exclude any term that is
a multiple of 4.

## Detailed Explanation

### Input format

Integer x

### Output format

Terms of series (separated by space)

### Constraints

$1 <= x <= 1,000$

```md
Sample Input 1:
10
Sample Output 1:
5 11 14 17 23 26 29 35 38 41
Sample Input 2:
4
Sample Output 2:
5 11 14 17
Explanation:
Input is 4 and print the first 4 numbers that are not divisible by 4 and are of the form 3N + 2, where k is a non-negative integer.
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
        int numOfTerms = sc.nextInt();
        int currentTerm, n = 1, termCount = 0;
        while(termCount < numOfTerms)
        {
            currentTerm = 3 * n + 2;
            if(currentTerm % 4 != 0)
            {
                System.out.print(currentTerm + " ");
                termCount++;
            }
            n++;
        }
    }
}
```
