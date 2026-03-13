# Categorizing Theme Park Visitors.md

## Problem Statement

Write a program for a theme park that categorizes visitors into four groups:
infants, children, adults, and seniors, based on their age. The program should
print a message indicating the category the visitor falls into.

**Categorize the visitor based on the following age groups:**

Infants: Age 0 to 4
Children: Age 5 to 12
Adults: Age 13 to 64
Seniors: Age 65 and above

## Detailed Explanation

### Input Format

The first line contains an Integer (age).

### Output format

Print the category of the visitor (Infants, Children, Adults and Seniors)

```md
Sample Input 1:
3
Sample Output 1:
Infants
Sample Input 2:
25
Sample Output 2:
Adults
```

## Solution

```java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        // write your code logic here !!
        Scanner sc = new Scanner(System.in);
        byte age = sc.nextByte();
        if(age >= 0 && age <= 4)
        {
            System.out.println("Infants");
        }
        else if(age >= 5 && age <= 12)
        {
            System.out.println("Children");
        }
        else if(age >= 13 && age <= 64)
        {
            System.out.println("Adults");
        }
        else
        {
            System.out.println("Seniors");
        }
    }
}
```
