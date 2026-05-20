# Set Matrix to Zero

## Problem Statement

You are given an N x M integer matrix. Your task is to modify this matrix in
place so that if any cell contains the value 0, then all cells in the same row
and column as that cell should also be set to 0.

### Requirements

- If a cell in the matrix has the value 0, set all other cells in that cell's row
and column to 0.

- You should perform this modification in place (without using additional
matrices).

- You must do it in place.

```ltf
For Example:

If the given grid is this:
[7, 19, 3]
[4, 21, 0]

Then the modified grid will be:
[7, 19, 0]
[0, 0,  0]
```

## Detailed Explanation

### Input Format

The first line of the input contains a single integer ‘T’ representing the no.
of test cases.

The first line of each test case contains two space-separated integers ‘N’ and
‘M’, denoting the no. of the rows and columns of the matrix.

The next 'N' lines will contain ‘M’ space separated integers representing the
elements of the matrix.

### Output Format

For each test case, print the modified grid.

Print output of each test case in a separate line.

**Note**: You are not required to print anything; it has already been taken
care of. Just implement the function and return the answer.

### Constraints

$1 ≤ T ≤ 1000$

$1 ≤ m, n ≤ 1000$

$Σ(m * n) ≤ 2000000$

$-2^(31) ≤ matrix[i][j] ≤ 2^(31)-1, for all (1 ≤ i ≤ n \ and\ 1 ≤ j ≤ m).$

Time Limit: $1 sec$

```ltf
Sample Input 1 :
2
2 3
7 19 3
4 21 0
3 3
1 2 3
4 0 6
7 8 9
Sample Output 1 :
7 19 0
0 0 0
1 0 3
0 0 0
7 0 9

Explanation For Sample Input 1, Case 2:
Only the cell (2,2) has zero. So all the elements of the second row and second
column are changed to zeros.

Sample Input 2 :
2
4 2
1 0
2 7
3 0
4 8
3 3
0 2 3
1 0 3
1 2 0
Sample Output 2 :
0 0
2 0
0 0
4 0
0 0 0
0 0 0
0 0 0
```

## Solution

```java
import java.io.*;
import java.util.* ;

public class Solution 
{
    public static void setZeros(int matrix[][]) 
    {
        // Write your code here..
        int n = matrix.length;
        int m = matrix[0].length;
        int[][] copy = getCopy(matrix);
        for(int i = 0; i < n; i++)
        {
            boolean isZeroInRow = false;
            for(int j = 0; j < m; j++)
            {
                if(copy[i][j] == 0)
                {
                    setColumnToZeroes(matrix, j);
                    isZeroInRow = true;
                }
            }
            if(isZeroInRow)
            {
                setRowToZeroes(matrix, i);
            }
        }
    }

    private static int[][] getCopy(int[][] matrix)
    {
        int[][] mat = new int[matrix.length][matrix[0].length];
        for(int i = 0; i < matrix.length; i++)
        {
            for(int j = 0; j < matrix[0].length; j++)
            {
                mat[i][j] = matrix[i][j];
            }
        }
        return mat;
    }

    private static void setRowToZeroes(int[][] matrix, int row)
    {
        for(int col = 0; col < matrix[row].length; col++)
        {
            matrix[row][col] = 0;
        }
    }

    private static void setColumnToZeroes(int[][] matrix, int col)
    {
        for(int row = 0; row < matrix.length; row++)
        {
            matrix[row][col] = 0;
        }
    }
}
```
