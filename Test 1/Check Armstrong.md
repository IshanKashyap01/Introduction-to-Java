# Check Armstrong

```Java
import java.util.Scanner;

public class Main 
{    
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int k = 1;
        for(int i = n / 10; i > 0; i /= 10)
        {
            k++;
        }
        int num = 0, digit;
        for(int i = n; i > 0; i /= 10)
        {
            num += (int) Math.pow(i % 10, k);
        }
        System.out.println(num == n);
    }
}
```
