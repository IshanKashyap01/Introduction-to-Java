# Square Matrix

## Problem Statement

You are given a 2D array of integers ‘A’ of length ’N’x’M’, where ‘N’ is the
number of rows and ‘M’ is the number of columns. Check if the given array forms
a square matrix and returns its diagonal elements.

A Square matrix is one that has an equal number of rows and columns.

## Detailed Explanation

### Input Format

The first line of the input contains an integer 'T’, Denoting the number of
test cases.

The first line of each test case contains two integers ‘N’ and ‘M’ separated by
space.

The next ’N’ lines in each test contain ‘M’ integers separated by space.

### Output format

Return a pair of strings and an array, If the matrix is a square matrix, return
‘YES’with the array containing the diagonal elements, else return ‘NO’ with an
empty array.

### Constraints

$1  <= T <= 10$

$1  <= N,M <= 50$

$1 <= A[i] <= 1000$

Time Limit: $1 sec$

```ltf
Sample Input 1:
2
3 3
1 2 3
4 5 6
7 8 9
2 3
1 3 2 
4 5 5
Sample Output 1:
YES
1 5 9
NO

Explanation Of Sample Input 1 :
Test 1:
The number of rows and columns is equal, so the given array forms a square
matrix.
Test 2:
The number of rows and columns is not equal, so the given array doesn’t form a
square matrix.

Sample Input 2 :
2
2 2
1 2
2 1
1 1
3
Sample Output 2 :
YES
1 1
YES
3
```

## Solution

```java
import java.util.*;

public class Solution 
{
    public static String sqrMat(int [][]mat, int n, int m,int diag[]) 
    {
        // Write your code here.
        if(n != m)
        {
            return "NO";
        }
        for(int i = 0; i < n; i++)
        {
            diag[i] = mat[i][i];
        }
        return "YES";
    }
}
```
