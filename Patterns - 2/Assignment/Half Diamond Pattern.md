# Half Diamond Pattern

```Java
import java.util.Scanner;

public class Solution 
{    
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        System.out.println('*');
        for(int i = 1; i <= n; i++)
        {
            System.out.print('*');
            for(int j = 1; j <= i; j++)
            {
                System.out.print(j);
            }
            for(int d = i - 1; d >= 1; d--)
            {
                System.out.print(d);
            }
            System.out.println('*');
        }
        for(int i = 1; i <= n - 1; i++)
        {
            System.out.print('*');
            for(int j = 1; j <= n - i; j++)
            {
                System.out.print(j);
            }
            for(int d = n - i - 1; d >= 1; d--)
            {
                System.out.print(d);
            }
            System.out.println('*');
        }
        System.out.println('*');
    }
}
```
