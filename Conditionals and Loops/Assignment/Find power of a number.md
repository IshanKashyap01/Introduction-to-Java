# Find power of a number

```Java
import java.util.Scanner;

public class Solution 
{
    public static void main(String[] args) 
    {
        // Write your code here    
        Scanner sc = new Scanner(System.in);
        int x = sc.nextInt(), n = sc.nextInt();
        int ans = 1;
        for(int i = 1; i <= n; i++)
        {
            ans *= x;
        }
        System.out.print(ans);
    }
}
```
