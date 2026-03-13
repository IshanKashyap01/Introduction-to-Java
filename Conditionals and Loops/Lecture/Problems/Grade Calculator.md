# Grade Calculator

## Problem Statement

Your program should take an integer input representing the numerical score and
output the corresponding grade. If the input score is not within the valid
range (0-100), the program should display "Invalid score".

### Instructions

The grading system is as follows:

A: 90-100
B: 80-89
C: 70-79
D: 60-69
F: 0-59

### Detailed Explanation

#### Input format

The first line of input contains An integer score (0 <= score <= 100)
representing the numerical score.

#### Output format

The first line of output contains a string representing the grade or "Invalid score."

```md
Sample Input 1:
-1 
Sample Output 1:
Invalid score
Sample Input 2:
85 
Sample Output 2:
B
Sample Input 3:
10 
Sample Output 3:
F
```

## Solution

```java
import java.util.Scanner;

public class Solution 
{
   public static void main(String[] args)
   {
      // write your code ..
      Scanner sc = new Scanner(System.in);
      int score = sc.nextInt();
      if(score >= 90 && score <= 100)
      {
         System.out.println('A');         
      }
      else if(score >= 80 && score < 90)
      {
         System.out.println('B');
      }
      else if(score >= 70 && score < 80)
      {
         System.out.println('C');
      }
      else if(score >= 60 && score < 70)
      {
         System.out.println('D');
      }
      else if (score >= 0 && score < 60)
      {
         System.out.println('F');
      }
      else
      {
         System.out.println("Invalid score");
      }
   }
}
```
