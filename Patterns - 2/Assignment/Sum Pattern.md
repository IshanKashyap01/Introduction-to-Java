# Sum Pattern

```Java
import java.util.Scanner;

public class Solution 
{    
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int sum;
        for(int i = 1; i <= n; i++)
        {
            sum = 1;
            System.out.print(1);
            for(int j = 2; j <= i; j++)
            {
                System.out.print("+" + j);
                sum += j;
            }
            System.out.println("=" + sum);
        }
    }
}
```
