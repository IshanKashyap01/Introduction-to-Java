# Inverted Number Pattern

```Java
import java.util.*;

public class Solution 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        for(int i = 1; i <= n; i++)    
        {
            for(int j = 0; j <= n - i; j++)
            {
                System.out.print(n - i + 1);
            }
            System.out.println();
        }
    }
}
```
