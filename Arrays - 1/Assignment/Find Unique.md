# Find Unique

```Java
public class Solution
{  

    public static int findUnique(int[] arr)
    {
        int num = 0;
        for(int i : arr)
        {
          num ^= i;
        }
        return num;
    }
}
```
