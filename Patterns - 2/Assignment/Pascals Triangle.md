# Pascal's Triangle

## Problem Statement

You are given an integer N. Your task is to print the pascal’s triangle till
the row N.

A Pascal's triangle is a triangular array constructed by summing adjacent
elements in preceding rows. Pascal's triangle contains the values of the
binomial coefficient. For example in the figure below.

For example, given integer N= 4 then you have to print.

1  
1 1  
1 2 1  
1 3 3 1

Here for the third row, you will see that the second element is the summation
of the above two-row elements i.e. `2 = 1 + 1`, and similarly for row three
`3 = 1 + 2` and `3 = 1 + 2`.

## Detailed Explanation

### Input format

A single integer N is provided as input denoting the row till which you have to
print the pascal’s triangle.

### Output format

Print N rows of Pascal’s Triangle, where each row is printed on a new line with
leading spaces to maintain the triangular format.

### Note

The output must be printed directly to standard output.

No extra spaces or blank lines should be added after the final row.

The format of spaces and numbers should exactly match the expected pattern to
pass the test cases.

### Constraints

$1 <= N <= 50$

```ltf
Time Limit: 1 sec
Sample Input 1 :
3
Sample Output 1:
  1
 1 1
1 2 1
Sample Input 1 :
6
Sample Output 2 :
     1
    1 1
   1 2 1
  1 3 3 1
 1 4 6 4 1
1 5 10 10 5 1
```

## Solution

```java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
       // write your code logic !!
       Scanner sc = new Scanner(System.in);
       byte rows = sc.nextByte();
       for(byte row = 1; row <= rows; row++)
       {
           // There are n - i spaces every row
           for(byte spaces = 0; spaces < rows - row; spaces++)
           {
              System.out.print(' ');
           }
           for(int column = 1, prev = 1; column <= row; column++)
           {
               System.out.print(prev + " ");
               // Formula for element at (i, j) in Pascal's triangle
               prev = prev * (row - column) / column;
           }
           System.out.println();
       }
    }
}
```

### Explanation

The formula for the value at `j`th column of `i`th row for Pascal's triangle:

$$
C(i, j) = C(i, j - 1) \cdot \frac{(i - j)}{j}
$$
