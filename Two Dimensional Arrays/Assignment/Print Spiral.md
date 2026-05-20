# Print Spiral

## Problem Statement

For a given two-dimensional integer array/list of size (N x M), print it in a
spiral form. That is, you need to print in the order followed for every
iteration:

1. First row(left to right)

2. Last column(top to bottom)

3. Last row(right to left)

4. First column(bottom to top)

Mind that every element will be printed only once.

**refer to the image below**:

![a 5x6 spiral array](https://files.codingninjas.in/0000000000004006.jpeg)

## Detailed Explanation

### Input format

The first line contains an Integer 't' which denotes the number of test cases
or queries to be run. Then the test cases follow.

First line of each test case or query contains two integer values, 'N' and 'M',
separated by a single space. They represent the 'rows' and 'columns'
respectively, for the two-dimensional array/list.

Second line onwards, the next 'N' lines or rows represent the ith row values.

Each of the ith row constitutes 'M' column values separated by a single space.

### Output format

For each test case, print the elements of the two-dimensional array/list in the
spiral form in a single line, separated by a single space.

Output for every test case will be printed in a separate line.

### Constraints

$1 <= t <= 10^2

0 <= N <= 10^3

0 <= M <= 10^3$

Time Limit: $1 sec$

```ltf
Sample Input 1:
1
4 4 
1 2 3 4 
5 6 7 8 
9 10 11 12 
13 14 15 16
Sample Output 1:
1 2 3 4 8 12 16 15 14 13 9 5 6 7 11 10 
Sample Input 2:
2
3 3 
1 2 3 
4 5 6 
7 8 9
3 1
10
20
30
Sample Output 2:
1 2 3 6 9 8 7 4 5 
10 20 30 
```

## Solution

```Java
public class Solution 
{
    public static void spiralPrint(int matrix[][])
    {
        //Your code goes here
        if(matrix.length == 0)
        {
            return;
        }
        int left = 0, right = matrix[0].length - 1;
        int top = 0, bottom = matrix.length - 1;
        while(left <= right && top <= bottom)
        {
            // top-left to top-right
            for(int i = left; i <= right; i++)
            {
                System.out.print(matrix[top][i] + " ");
            }
            top++;
            // top-right to bottom-right
            for(int i = top; i <= bottom; i++)
            {
                System.out.print(matrix[i][right] + " ");
            }
            right--;
            // bottom-right to bottom-left
            if(top <= bottom)
            {
                for(int i = right; i >= left; i--)
                {
                    System.out.print(matrix[bottom][i] + " ");
                }
                bottom--;
            }
            // bottom-left to top-left
            if(left <= right)
            {
                for(int i = bottom; i >= top; i--)
                {
                    System.out.print(matrix[i][left] + " ");
                }
                left++;
            }
        }
    }
}
```
