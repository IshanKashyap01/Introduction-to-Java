# Push Zeros to end

## Problem Statement

Given an array 'arr' of 'n' non-negative integers, your task is to move all the
zeros to the end of the array while keeping the non-zero elements at the start
of the array in their original order. Return the modified array.

**Example**:

Input: ‘n’ = 5, ‘arr’ = [1, 2, 0, 0, 2, 3]

Output: [1, 2, 2, 3, 0, 0]

Explanation: Moved all the 0’s to the end of an array, and the rest of the
elements retain the order at the start.

## Detailed Explanation

### Input Format

The first line contains an integer ‘n’, the number of elements in the array
‘arr’.

The next line contains the 'n' space-separated integers of the array 'arr'.

### Output Format

The output contains the elements of the modified array separated by space.

**Note**:

You are not required to print anything; it has already been taken care of. Just
implement the function.

### Constraints

$1 ≤ n ≤ 10^6$

$0 ≤ arr[i] ≤ 10^9$

Time limit: $1 sec$

```ltf
Sample input 1:
4
0 0 0 1 
Sample output 1:
1 0 0 0 
Explanation of sample input 1:
Output: [1, 0, 0, 0]

We move all the 0’s to the end of an array, and the rest of the elements retained the order at the start.
Sample input 2:
5
4 0 3 2 5 
Sample output 2:
4 3 2 5 0 
Explanation of sample input 2:
Output: [4, 3, 2, 5, 0]

we move all the 0’s to the end of an array, and the rest of the elements retained the order at the start.
```

## Solution

```java
public class Solution 
{
    public static int[] moveZeros(int n, int[] arr) 
    {
        // To keep track of where the next non-zero number should be placed
        int nonZeroIndex = 0;
        // Start the loop with 0 as there may be a non-zero number at the start, in which
        // case the swap will change nothing
        for(int i = 0; i < n; i++)
        {
            // if a non-zero value is spotted, swap it to the right place
            if(arr[i] != 0)
            {
                // non-zero index will move one place forward
                swapElementsInArray(arr, i, nonZeroIndex++);
            }
        }
        return arr;
    }

    public static void swapElementsInArray(int[] arr, int i, int j)
    {
        int temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }
}
```

**Note**: The algorithm used above is called *stable compaction* and used when
the relative order of selected elements must remain the same.
