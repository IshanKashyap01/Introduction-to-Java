# Lowercase

## Problem Statement

You are provided with a sentence in all upper case. Your task is to convert it into lower case and print it .

**Note: Use the inbuilt method provided under the wrapper class for String.**

## Instructions

1. We have already declared a sentence in upper case.

2. You have to convert it into lower case and print it.

## Detailed Explanation

### Input format

The first line of the input contains a sentence in upper case.

### Output format

The first line of the output should print the sentence in lower case.

```md
Sample Input:
I AM LEARNING FUNDAMENTALS OF JAVA
Sample Output:
i am learning fundamentals of java
```

## Solution

```java
public class ConvertToLowerCase
{
    public static void main(String[] args) 
    {    
        String upperCaseString = "I AM LEARNING FUNDAMENTALS OF JAVA";
        //Convert the above given string into all lowercase using wrapper class method of String
        //Use inbuilt feature of String .toLowerCase()
        //Print the newly converted lower case string.
        System.out.println(upperCaseString.toLowerCase());        
    }
}
```
