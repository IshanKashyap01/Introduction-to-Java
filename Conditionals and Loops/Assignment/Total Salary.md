# Total Salary

## Problem Statement

Write a program to calculate the total salary of a person. The user has to
enter the basic salary (an integer) and the grade (an uppercase character),
depending upon which the total salary is calculated as:

```md
Total_salary = Basic + HRA + DA + Allow – PF
where:  
HRA   = 20% of basic  
DA    = 50% of basic  
Allow = 1700 if grade = ‘A’  
Allow = 1500 if grade = ‘B’  
Allow = 1300 if grade = ‘C' or any other character  
PF    = 11% of basic.  
```

**Round off the total salary and then print the integral part only.**

## Detailed Explanation

### Input format

Basic salary & Grade (separated by space)

### Output Format

Total Salary

### Constraints

$0<=salary<=10000$

```md
Sample Input 1 :
10000 A
Sample Output 1 :
17600
Sample Input 2 :
4567 B
Sample Output 2 :
8762

Explanation of Input 2:

We have been given the basic salary as Rs. 4567. We need to calculate the hra, da and pf. 
Now when we calculate each of the, it turns out to be:
hra =  20% of Rs. 4567 = Rs. 913.4
da = 50% od Rs. 4567 = Rs. 2283.5
pf = 11% of Rs. 4567 = Rs. 502.37

Since, the grade is 'B', we take allowance as Rs. 1500.
On substituting these values to the formula of totalSalary, we get Rs. 8761.53 and now rounding it off will result in Rs. 8762 and hence the Answer.
```

## Solution

```java
import java.util.Scanner;

public class Solution
{
    public static void main(String[] args) 
    {
        //Write your code here. 
        // Math.round() An internal function implemented in the
        // Math class(no need to import as it is available as default) to round off the decimal values
        Scanner sc = new Scanner(System.in);
        int basic = sc.nextInt();
        char grade = sc.next().charAt(0);
        // basic (1) + HRA (0.2) + DA (0.5) - PF (0.11) = 1.59
        double total = 1.59 * basic;
        total += switch(grade)
        {
            case 'A' -> 1700;
            case 'B' -> 1500;
            default -> 1300;
        };
        System.out.println(Math.round(total));
    }
}
```
