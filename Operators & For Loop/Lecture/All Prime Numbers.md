# All Prime Numbers

```Java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        boolean flag;
        for(int i = 2; i <= n; i++)
        {
            flag = true;
            for(int j = 2; j <= i / 2; j++)
            {
                if(i % j == 0)
                {
                    flag = false;
                    break;
                }
            }
            if(flag)
            {
                System.out.println(i);
            }
        }
    }
}
```
