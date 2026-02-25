# Simple Interest

## Problem Statement

Take the principal amount, rate of interest, and the time period as input and
calculate the Simple Interest.

Note: Print the answer as **integer value**.

### Detailed Explanation

#### Input Format

- The first line of input contains a single integer Principal amount.

- The Second line of input contains a single decimal Rate of interest.

- The Third line of input contains a single Integer Time period.

#### Output Format

Calculate the Simple Interest and print it.

```md
Sample Input 1:
2000
2.2
4
Sample Output 1:
176
Explanation:
principal=2000,rate=2.2 and time=4.
Simple interest = (Principal*rate*time) /100
Hence answer is (2000*2.2*4)/100 = 176
```

## Solution

```java
import java.util.* ;
import java.io.*; 
class Solution
{
    public static void main(String args[]) 
    {
        // Write code here
        Scanner scanner = new Scanner(System.in);
        int principal = scanner.nextInt();
        float rate = scanner.nextFloat();
        int time = scanner.nextInt();
        int simpleInterest = (int) ((principal * rate * time) / 100);
        System.out.println(simpleInterest);
    }
}
```
