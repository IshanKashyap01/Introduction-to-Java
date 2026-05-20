# Largest Row or Column

## Problem Statement

You are given a 2D list (array) with dimensions N rows and M columns, filled
with integers. Your task is to find the row or column that has the largest sum
of its elements.

**Important Rules**:

- If two or more rows/columns have the same sum, choose the one that comes
first.

- If a row and a column have the same largest sum, choose the row.

**Goal**: Return which row or column has the largest sum.

## Detailed Explanation

### Input Format

The first line contains an Integer 't' which denotes the number of test cases
or queries to be run. Then the test cases follow.

First line of each test case or query contains two integer values, 'N' and 'M',
separated by a single space. They represent the 'rows' and 'columns'
respectively, for the two-dimensional array/list.

Second line onwards, the next 'N' lines or rows represent the ith row values.

Each of the ith row constitutes 'M' column values separated by a single space.

### Output Format

For each test case, If row sum is maximum, then print: "row"
`<row_index> <row_sum>`

OR

If column sum is maximum, then print: "column" `<col_index> <col_sum>`

It will be printed in a single line separated by a single space between each
piece of information.

Output for every test case will be printed in a separate line.

**Consider**: If there doesn't exist a sum at all then print
`row 0 -2147483648`, where `-2147483648` or `-2^31` is the smallest value for
the range of Integer.

### Constraints

$1 <= t <= 10^2$

$1 <= N <= 10^3$

$1 <= M <= 10^3$

Time Limit: $1 sec$

```ltf
Sample Input 1:
1
3 2
6 9 
8 5 
9 2 
Sample Output 1:
column 0 23
Sample Input 2:
1
4 4
6 9 8 5 
9 2 4 1 
8 3 9 3 
8 7 8 6 
Sample Output 2:
column 0 31
```

## Solution

```Java
public class Solution 
{
    public static void findLargest(int mat[][])
    {
        int[] row = largestRow(mat);
        int[] col = largestColumn(mat);
        if(row[1] >= col[1])
        {
            System.out.println("row " + row[0] + " " + row[1]);
        }
        else
        {
            System.out.println("column " + col[0] + " " + col[1]);
        }
    }

    public static int[] largestRow(int[][] mat)
    {
        int row = 0, max = Integer.MIN_VALUE;
        for(int i = 0, sum = 0; i < mat.length; i++, sum = 0)
        {
            for(int j = 0; j < mat[0].length; j++)
            {
                sum += mat[i][j];
            }
            if(sum > max)
            {
                max = sum;
                row = i;
            }
        }
        return new int[]{row, max};
    }

    private static int[] largestColumn(int[][] mat)
    {
        int col = 0, max = Integer.MIN_VALUE;
        if(mat.length == 0)
        {
            return new int[]{col, max};
        }
        for(int j = 0, sum = 0; j < mat[0].length; j++, sum = 0)
        {
            for(int i = 0; i < mat.length; i++)
            {
                sum += mat[i][j];
            }
            if(sum > max)
            {
                max = sum;
                col = j;
            }
        }
        return new int[]{col, max};
    }
}
```
