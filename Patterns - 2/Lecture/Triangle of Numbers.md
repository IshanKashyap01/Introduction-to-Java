# Triangle of Numbers

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
            for(int s = 1; s <= n - i; s++)
            {
                System.out.print(" ");
            }
            for(int j = 1; j <= i; j++)
            {
                System.out.print(i + j - 1);
            }
            for(int d = i - 1; d >= 1; d--)
            {
                System.out.print(i + d - 1);
            }
            System.out.println();
        }
    }
}
```
