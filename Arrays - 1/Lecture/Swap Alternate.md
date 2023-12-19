# Swap Alternate

```Java
public class Solution 
{    
    public static void swapAlternate(int arr[]) 
    {
        for(int i = 0, j = 1; j < arr.length; i += 2, j += 2)
        {
            swap(i, j, arr);
        }
    }

    public static void swap(int i, int j, int[] arr)
    {
        arr[i] += arr[j];
        arr[j] = arr[i] - arr[j];
        arr[i] -= arr[j];
    }
}
```
