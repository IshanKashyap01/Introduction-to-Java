# Diamond of stars

```Java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int x = (n / 2) + 1, y = n / 2;
        for(int i = 1; i <= x; i++)        
        {
            for(int s = 1; s <= x - i; s++)
            {
                System.out.print(" ");
            }
            for(int j = 1; j <= i; j++)
            {
                System.out.print("*");
            }
            for(int d = i - 1; d >= 1; d--)
            {
                System.out.print("*");
            }
            System.out.println();
        }
        for(int i = 1; i <= y; i++)
        {
            for(int s = 1; s <= i; s++)
            {
                System.out.print(" ");
            }
            for(int j = 1; j <= y - i + 1; j++)
            {
                System.out.print("*");
            }
            for(int d = y - i; d >= 1; d--)
            {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```
