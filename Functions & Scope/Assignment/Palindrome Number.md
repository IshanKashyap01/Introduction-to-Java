# Palindrome Number

Check whether a given number ’n’ is a palindrome number.

**Note:**

Palindrome numbers are the numbers that don't change when reversed.
You don’t need to print anything. Just implement the given function.

**Example:**

Input: 'n' = 51415
Output: true
Explanation: On reversing, 51415 gives 51415.

## Detailed Explanation

### Input Format

The first and only line of the input contains the number 'n'.

### Output format

Return a boolean value True or False.

### Constraints

$1 <= n <= 10^9$

```ltf
Time Limit: 1 sec
Sample Input 1:
1032
Sample Output 1:
false
Explanation Of Sample Input 1:
1032, on being reversed, gives 2301, which is a totally different number.
Sample Input 2:
121
Sample Output 2:
true
Explanation Of Sample Input 2:
121, on being reversed, gives 121, which is the same.
Expected time complexity:
The expected time complexity is O(log(n)).
```

## Solution

```java
import java.util.Scanner;

public class Solution 
{   
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int number = sc.nextInt();
        System.out.print(number == reverse(number));
    }

    public static int reverse(int number)
    {
        int reverse = 0;
        while(number > 0)
        {
            reverse = reverse * 10 + number % 10;
            number /= 10;
        }
        return reverse;
    }
}
```
