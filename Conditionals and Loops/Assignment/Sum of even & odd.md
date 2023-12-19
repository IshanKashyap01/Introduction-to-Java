# Sum of even & odd

```Java
import java.util.*;

public class Main 
{
    public static void main(String[] args) 
    {
        // Write your code here
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int even = 0, odd = 0;
        int temp;
        while(num != 0)
        {
            temp = num % 10;
            if(temp % 2 == 0)
            {
                even += temp;
            }
            else
            {
                odd += temp;
            }
            num /= 10;
        }
        System.out.print(even + " " + odd);
    }
}
```
