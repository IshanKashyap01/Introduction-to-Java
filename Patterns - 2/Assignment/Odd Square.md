# Odd Square

```Java
import java.util.Scanner;

public class Main 
{    
    public static void main(String[] args) 
    {
        // Write your code here
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int x, y;
        for(int i = 1; i <= n; i++)
        {
            x = i * 2 - 1;
            for(int j = 1; j <= n - i + 1; j++)
            {
                System.out.print(x);
                x += 2;
            }
            y = 1;
            for(int d = i - 1; d >= 1; d--)
            {
                System.out.print(y);
                y += 2;
            }
            System.out.println();
        }
    }
}
```
