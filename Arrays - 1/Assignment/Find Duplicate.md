# Find Duplicate

```Java
public class Solution
{    
    public static int duplicateNumber(int arr[]) 
    {
        int num = 0;
        for(int i = 0; i < arr.length; i++)
        {
            for(int j = i + 1; j < arr.length; j++)
            {
                if(arr[i] == arr[j])
                {
                    return arr[i];
                }
            }
        }
        return -1;
    }
}
```
