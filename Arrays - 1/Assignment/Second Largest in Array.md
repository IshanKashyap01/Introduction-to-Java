# Second Largest In Array

You have been given a random integer array/list(ARR) of size N. You are
required to find and return the second largest element present in the
array/list.

## Detailed Explanation

### Input format

The first line contains an integer 'N' representing the size of the array/list.

The second line contains 'N' single space separated integers representing the elements in the array/list.

### Output Format

Return the second largest element in the array/list.

### Constraints

$0 <= N <= 10^2$

$1<=arr[i]<=10^3$

Time Limit: $1 sec$

```ltf
Sample Input 1:
5
4 3 10 9 2
Sample Output 1:
9
Sample Input 2:
7
13 6 31 14 29 44 3
Sample Output 2:
31
```

## Solution

```java
public class Solution 
{  
    public static int secondLargestElement(int[] arr, int n) 
    {
        if(n == 0)
        {
            return 0;
        }
        int max1 = arr[0], max2 = arr[0];
        for(int i = 1; i < n; i++)
        {
            if(arr[i] > max1)
            {
                if(max1 > max2)
                {
                    max2 = max1;
                }
                max1 = arr[i];
            }
            else if(arr[i] > max2)
            {
                max2 = arr[i];
            }
        }
        return max2;
    }
}
```
