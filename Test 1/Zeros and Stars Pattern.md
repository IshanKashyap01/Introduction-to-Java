# Zeros and Stars Pattern

```Java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        for(int i = 1; i <= n; i++)        
        {
            for(int j = 1; j <= n; j++)
            {
                System.out.print(j == i ? "*" : 0);
            }
            System.out.print('*');
            for(int j = 1; j <= n; j++)
            {
                System.out.print(j == n - i + 1 ? "*" : 0);
            }
            System.out.println();
        }
    }
}
```
