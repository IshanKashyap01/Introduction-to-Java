# Terms of AP

```Java
import java.util.Scanner;

public class Main 
{    
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int x = sc.nextInt();
        int i = 1, n = 1, num;
        while(i <= x)
        {
            num = 3 * n + 2;
            if(num % 4 != 0)
            {
                System.out.print(num + " ");
                i++;
            }
            n++;
        }
    }
}
```
