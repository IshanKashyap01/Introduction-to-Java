# Binary to decimal

```Java
import java.util.Scanner;

public class Main 
{    
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int num = 0, m = 1;
        while(n > 0)
        {
            if(n % 10 == 1)
            {
                num += m;
            }
            m *= 2;
            n /= 10;
        }
        System.out.println(num);
    }
}
```
