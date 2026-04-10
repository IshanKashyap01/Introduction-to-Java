# Reverse String Word-wise

## Problem Statement

Aadil has been provided with a sentence in the form of a string as a function
parameter. The task is to implement a function so as to change the sentence
such that each word in the sentence is reversed. A word is a combination of
characters without any spaces.

Example:

Input Sentence: "Hello I am Aadil"

The expected output will look, "olleH I ma lidaA".

## Detailed Explanation

### Input Format

The first and only line of input contains a string without any leading and
trailing spaces. The input string represents the sentence given to Aadil.

### Output Format

You don't need to print anything just change the sentence(string) such that
each word in the sentence is reversed.

### Constraints

$0 <= N <= 10^6$

Where N is the length of the input string.

All the words in string are separated by a single space.

String does not contain any leading or trailing spaces.

Time Limit: $1 sec$

```ltf
Sample Input 1:
Welcome to Coding Ninjas
Sample Output 1:
emocleW ot gnidoC sajniN
Sample Input 2:
Always indent your code
Sample Output 2:
syawlA tnedni ruoy edoc
```

## Solution

```Java
public class Solution 
{
    public static String reverseEachWord(String str) 
    {
        //Your code goes here
        String[] words = str.split(" ");
        String reverseSentence = "";
        for(int i = 0; i < words.length - 1; i++)
        {
            reverseSentence += reverse(words[i]) + " ";
        }
        reverseSentence += reverse(words[words.length - 1]);

        return reverseSentence;
    }

    public static String reverse(String word)
    {
        char[] arr = new char[word.length()];
        for(int i = 0, j = word.length() - 1; i < word.length(); i++, j--)
        {
            arr[i] = word.charAt(j);
        }
        return new String(arr);
    }
}
```
