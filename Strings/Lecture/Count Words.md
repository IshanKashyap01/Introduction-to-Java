# Count Words

## Problem Statement

For a given input string(str), find and return the total number of words
present in it.

It is assumed that two words will have only a single space in between. Also,
there wouldn't be any leading and trailing spaces in the given input string.

## Detailed Explanation

### Input Format

The first and only line of input contains a string without any leading and
trailing spaces.

### Output Format

The only line of output prints an integer value denoting the tool number of
words present in the string.

**Note**: You are not required to print anything. It has already been taken
care of.

### Constraints

$0 <= N <= 10^6$

Where N is the length of the input string.

Time Limit: $1 sec$

```ltf
Sample Input 1:
Coding Ninjas!
Sample Output 1:
2
Sample Input 2:
this is a sample string
Sample Output 2:
5
```

## Solution

```Java
public class Solution 
{
    public static int countWords(String str) 
    {   
        //Your code goes here
        if(str.length() == 0)
        {
            return 0;
        }
        int words = 1;
        for(int i = 0; i < str.length(); i++)
        {
            words += str.charAt(i) == ' ' ? 1 : 0;
        }
        return words;
    }
}
```

**Note**: This code will return 2 if the input is ` `, which, although wrong,
is the desired output in this case.
