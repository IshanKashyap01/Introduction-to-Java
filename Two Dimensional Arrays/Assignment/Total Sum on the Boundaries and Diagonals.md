# Total Sum on the Boundaries and Diagonals

## Problem Statement

You are given a two-dimensional square matrix of size N×N. You need to find the
sum of the elements on:

1. The main diagonal (from the top-left corner to the bottom-right corner)

2. The secondary diagonal (from the top-right corner to the bottom-left corner)

3. All the boundary elements of the matrix

Make sure that no element is counted more than once, even if it belongs to both
diagonals or is a boundary element. Your task is to compute the sum of all
these unique elements.

## Detailed Explanation

### Input format

The first line contains an Integer 't' which denotes the number of test cases
or queries to be run. Then the test cases follow.

First line of each test case or query contains a single integer value, 'N'
representing the 'rows' and 'columns' for the two-dimensional square matrix.

Second line onwards, the next 'N' lines or rows represent the ith row values.

Each of the ith row constitutes 'N' column values separated by a single space.

### Output format

For each test case, print the single integer denoting the sum.

Output for every test case will be printed in a separate line.

### Constraints

$1 <= t <= 10^2$

$0 <= N <= 10^3$

Time Limit: $1 sec$

```ltf
Sample input 1:
1
3
1 2 3
4 5 6
7 8 9
Sample Output 1:
45

Explanation for Sample Output 1:
The boundary elements are 1, 2, 3, 6, 9, 8, 7 and 4. 

The first-diagonal elements are 1, 5 and 9. 

The second-diagonal elements are 3, 5 and 7.

We just need to add all these numbers making sure that no number is added
twice. For example, '1' is both a boundary element and a first-diagonal element
similarly, '5' contributes to both the diagonals but they won't be added twice.

Hence, we add up, [1 + 2 + 3 + 6 + 9 + 8 + 7 + 4 + 5] to give 45 as the output.

Sample input 2:
2
5
1 2 3 4 5
6 7 8 9 10
11 12 13 14 15
16 17 18 19 20
21 22 23 24 25
4
1 2 3 10
4 5 6 11
7 8 9 12
13 14 15 16
Sample Output 2:
273
136
```

## Solution

```Java
public class Solution 
{
    public static void totalSum(int[][] mat) 
    {
        //Your code goes here
        int sum = 0, n = mat.length - 1;
        for(int start = 0, end = n; start <= n; start++, end--)
        {
            // rows
            sum += mat[0][start] + mat[n][start];
            if(start > 0 && start < n)
            {
                // columns
                sum += mat[start][0] + mat[start][n];
                // main diagonal
                sum += mat[start][start];
                // secondary diagonal
                sum += start != end ? mat[start][end] : 0;
            }
        }
        System.out.println(sum);
    }
}
```
