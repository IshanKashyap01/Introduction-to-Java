# Nth Fibonacci Number

```Java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int n1 = 0, n2 = 1;
        int num = 1;
        for(int i = 1; i < n; i++)
        {
            num = n1 + n2;
            n1 = n2;
            n2 = num;
        }
        System.out.println(num);
    }
}
```
