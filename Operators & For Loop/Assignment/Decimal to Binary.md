# Decimal to Binary

```Java
import java.util.Scanner;

public class Main 
{    
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        long num = 0, pv = 1;
        while(n > 0)
        {
            num += (n % 2) * pv;
            n /= 2;
            pv *= 10;
        }
        System.out.println(num);
    }
}
```
