# Rotate Array

## Problem Statement

You are given an array A of size N.

You are also given an integer X and a direction DIR. You need to rotate the
array A by X positions in the direction specified by DIR.

DIR can be:

- 'LEFT': Rotate the array to the left by X positions.
- 'RIGHT': Rotate the array to the right by X positions.

Return the resulting rotated array.

For example:

Input:
A = [6, 2, 6, 1], X = 1, DIR = ‘LEFT’

Output:
2 6 1 6

Explanation: Rotate array ‘A’ to the left one time.
[6, 2, 6, 1] => [2, 6, 1, 6]

## Detailed Explanation

### Input Format

First-line contains 'T,' denoting the number of Test cases.

For each Test case:

The first line contains two integers, ‘N', ‘X’, and the string ‘DIR’.

The second line has ‘N’ integers denoting the array ‘A’.

### Output Format

You must return the rotated array.

**Note**: You don’t need to print anything. Just implement the given function.

### Constraints

$1 <= T <= 10$

$1 <= N <= 10^5 $

$1 <= X <= 10^9$

‘DIR’ is an element of `{‘LEFT’, ‘RIGHT’}`

Time Limit: $1 sec$

```ltf
Sample Input 1 :
2
4 1 LEFT
1 2 3 4
6 2 RIGHT
1 2 4 3 5 6 
Sample Output 1 :
2 3 4 1
5 6 1 2 4 3
Explanation Of Sample Input 1 :
For test case one:

Input :
A = [1, 2, 3, 4], X = 1, DIR = ‘LEFT’

Output :
2 3 4 1

Explanation: Rotate array ‘A’ to the left one time.
[1, 2, 3, 4] => [2, 3, 4, 1]

For test case two:

Input :
A = [1, 2, 4, 3, 5, 6], X = 2, DIR = ‘RIGHT’

Output :
5 6 1 2 4 3

Explanation: Rotate array ‘A’ to the right one time.
[1, 2, 4, 3, 5, 6] => [6, 1, 2, 4, 3, 5]
Sample Input 2 :
2
6 3 LEFT
22 8 4 7 5 10
6 2 RIGHT
9 3 1 6 3 9
Sample Output 2 :
7 5 10 22 8 4 
3 9 9 3 1 6 
```

## Solution

```Java
public class Solution 
{
    public static int[] rotateArray(int []arr, int rotation, String dir) 
    {
        // Write your code here
        int n = arr.length;
        // If rotation is greater than length of array, it'll cause overflow
        rotation %= n;
        reverseArray(arr, 0, n - 1);
        if(dir.equals("RIGHT"))
        {
            reverseArray(arr, 0, rotation - 1);
            reverseArray(arr, rotation, n - 1);
        }
        else
        {
            reverseArray(arr, 0, n - rotation - 1);
            reverseArray(arr, n - rotation, n - 1);
        }
        return arr;
    }

    public static void reverseArray(int[] arr, int start, int end)
    {
        for(int i = start, j = end; i < j; i++, j--)
        {
            swapElementsInArray(arr, i, j);
        }
    }

    public static void swapElementsInArray(int[] arr, int i, int j)
    {
        int temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }
}
```

### Explanation

To rotate an array:

1. Reverse the array

2. If the rotation is to the right:

    a. Reverse the array from index `0` to `(rotation % length) - 1`

    b. Reverse the array from index `(rotation % length)` to `length - 1`

3. Else

    a. Reverse the array from index `0` to `length - (rotation % length) - 1`

    b. Reverse the array from index `length - (rotation % length)` to `length - 1`
