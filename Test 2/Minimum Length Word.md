# Minimum Length Word

## Problem Statement

Given a string S (that can contain multiple words), you need to find the word
which has minimum length.

Note : If multiple words are of same length, then answer will be first minimum
length word in the string. Words are separated by single space only.

## Detailed Explanation

### Input Format

String S

### Output Format

Minimum length word

### Constraints

$1 <= S <= 10^5$

```ltf
Sample Input 1:
this is test string
Sample Output 1:
is
Sample Input 2:
abc de ghihjk a uvw h j
Sample Output 2:
a
```

```Java
public class Solution 
{
    public static String minLengthWord(String input)
    {
        // Write your code here
        String[] words = input.split(" ");
        String smallest = words[0];
        for(String word : words)
        {
            smallest = word.length() < smallest.length() ? word : smallest;
        }
        return smallest;
    }
}
```
