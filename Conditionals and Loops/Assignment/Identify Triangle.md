# Identify Triangle

## Problem Statement

Given three positive integers as X, Y and Z representing three sides of a
triangle, write a program that determines whether the triangle formed by the
sides exist or not. If the triangle exists, classify it as isosceles, scalene
or equilateral.

**Condition for Triangle to exist:**

Sum of any two of its sides should be greater than the third side

## Detailed Explanation

### Input Format

Line 1: X(First Side)

Line 2: Y(Second Side)

Line 3: Z(Third Side)

### Output Format

First line of output prints "Not a Triangle"(If triangle doesn't exist) or
"Scalene/Isosceles/Equilateral Triangle" (If the triangle exists)

### Constraints

1<=X,Y,Z<=10^5

```md
Sample Input 1:
3
4
5
Sample Output 1:
Scalene Triangle
Explanation
As all three sides are different, so triangle is scalene.
Sample Input 2:
2
7
9
Sample Output 2:
Not a Triangle
```

## Solution

```java
import java.util.Scanner;

public class Solution
{
    public static void main(String[] args) 
    {
        // write your code logic here !!
        Scanner sc = new Scanner(System.in);
        int x = sc.nextInt();
        int y = sc.nextInt();
        int z = sc.nextInt();
        
        if(x + y > z && y + z > x && z + x > y)
        {
            if(x == y && y == z)
            {
                System.out.print("Equilateral");
            }
            else if(x == y || y == z || z == x)
            {
                System.out.print("Isosceles");
            }
            else
            {
                System.out.print("Scalene");
            }
            System.out.println(" Triangle");
        }
        else
        {
            System.out.println("Not a Triangle");
        }
    }
}
```
