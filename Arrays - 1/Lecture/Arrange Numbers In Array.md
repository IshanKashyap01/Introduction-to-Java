# Arrange Numbers In Array

```Java
public class Solution 
{    
    public static void arrange(int[] arr, int n) 
    {
        for(int i = 0, j = n - 1, k = 1; k <= n; k++)
        {
            if(k % 2 != 0)
            {
                arr[i++] = k;
            }
            else
            {
                arr[j--] = k;
            }
        }
    }
}
```
