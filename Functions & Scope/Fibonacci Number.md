# Fibonacci Number

```Java

public class Solution 
{    
    public static boolean checkMember(int n)
    {
        int f1 = 0, f2 = 1, f = 0;
        while(f < n)
        {
            f = f1 + f2;
            f1 = f2;
            f2 = f;
        }
        return f == n;
    }
}
```
