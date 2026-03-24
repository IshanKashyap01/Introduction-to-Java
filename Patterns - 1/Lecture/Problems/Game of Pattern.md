# Game of Pattern

## Problem Statement

Print the following pattern for the given N number of rows.  
**Pattern for N = 3**  
\###  
\###  
\###

## Detailed Explanation

### Input Format

Integer N (Total no. of rows)

### Output Format

Pattern in N lines

### Constraints

$0 <= N <= 50$

```md
Sample Input1:
5
Sample Output 1:
#####  
#####  
#####  
#####  
#####  
Sample Input 2:
4
Sample Output 2:
####  
####  
####  
####  
```

## Solution

```java
import java.util.*;

public class Solution
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int side = sc.nextInt();
        for(int row = 0; row < side; row++)
        {
            for(int column = 0; column < side; column++)
            {
                System.out.print('#');
            }
            System.out.println();
        }
    }
}
```
