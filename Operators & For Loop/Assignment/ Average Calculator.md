# Average Calculator

## Problem Statement

Your goal is to create a program called Average Calculator that takes three
integer inputs, calculates their average, and displays the result

### Detailed Explanation

#### Input Format

- The First line of input contains an integer variable 1.

- The Second line of input contains an integer variable 2.

- The Third line of input contains an integer variable 3.

#### Output Format

Calculate the Average and print it.

```md
Sample input 1:
1
2
3
Sample output 1:
2

Explanation:

We have a = 1,b = 2 and c = 3   
avg = (sum of elements ) / no of elements   
avg = (1+2+3)/3 =  6/3 = 2 

Sample input 2:
5
10
15
Sample output 2:
10
```

## Solution

```java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        Scanner scanner = new Scanner(System.in);
        //  take input 
        int v1 = scanner.nextInt();
        int v2 = scanner.nextInt();
        int v3 = scanner.nextInt();
        // write your logic ...
        System.out.println((v1 + v2 + v3) / 3);
    }
}
```
