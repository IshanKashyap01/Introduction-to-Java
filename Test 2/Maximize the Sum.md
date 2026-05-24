# Maximize the Sum

## Problem Statement

Given 2 sorted arrays (in increasing order), find a path through the
intersections that produces maximum sum and return the maximum sum.

That is, we can switch from one array to another array only at common elements.

If no intersection element is present, we need to take sum of all elements from
the array with greater sum.

## Detailed Explanation

### Input Format

Line 1: An integer M i.e. size of first array

Line 2: M integers which are elements of first array, separated by spaces

Line 3: An integer N i.e. size of second array

Line 4: N integers which are elements of second array, separated by spaces

### Output Format

Maximum sum value

### Constraints

$1 <= M, N <= 10^6$

```ltf
Sample Input:
6
1 5 10 15 20 25
5
2 4 5 9 15
Sample Output:
81
Explanation:
We start from array 2 and take sum till 5 (sum = 11). Then we'll switch to
array at element 10 and take till 15. So sum = 36. Now, no elements left in
array after 15, so we'll continue in array 1. Hence sum is 81
```

## Solution

```java
public class Solution 
{
    public static long maximumSumPath(int[] input1, int[] input2) 
    {
        long sum1 = 0, sum2 = 0, maxSum = 0;
        int i = 0, j = 0;
        // Traverse both arrays together
        while(i < input1.length && j < input2.length)
        {
            // The array with a smaller current number must have a few numbers
            // before it reaches the closest intersection point
            // input1 is behind
            if(input1[i] < input2[j])
            {
                sum1 += input1[i++];
            }
            // input2 is behind
            else if(input1[i] > input2[j])
            {
                sum2 += input2[j++];
            }
            // we're at the intersection point
            else
            {
                // use the bigger sum, add the intersection number and reset them both
                maxSum += Math.max(sum1, sum2) + input1[i];
                sum1 = sum2 = 0;
                i++;
                j++;
            }
        }
        // add the remaining numbers of whichever array is still left
        while(i < input1.length)
        {
            sum1 += input1[i++];
        }
        while(j < input2.length)
        {
            sum2 += input2[j++];
        }
        return maxSum + Math.max(sum1, sum2);
    }
}
```
