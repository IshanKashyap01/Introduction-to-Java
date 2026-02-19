# Average Marks

## Problem Statement

Given three integers, a, b and c. Create a program that calculates their
average and prints the result.

### Instructions

1. Declare an integer variable named sum and calculate the sum of the three
integers a, b, and c by adding them together.

2. Declare an int variable named average and calculate the average by dividing
the sum by 3 (the number of integers).

### Detailed Explanation

#### Input format

The first line of the input contains an integer "a".
The Second line of the input contains an integer "b".
The Third line of the input contains an integer "c ".

#### Output format

The first line of the output should print the average.

```md
Sample input 1:
1
2
3
Sample output 1:
2
Explanation :
avg = (sum of elements ) / no of elements
avg = (a+b+c)/3 =( 1+2+3)/3 = 6/3 = 2
Hence the output will be 2.
```

## Solution

```Java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);

        System.out.println(sc.next().charAt(0));
        System.out.print((sc.nextInt() + sc.nextInt() + sc.nextInt()) / 3);
    }
}
```
