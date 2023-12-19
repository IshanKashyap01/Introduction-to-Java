# Push Zeros to end

```Java
public class Solution 
{
    public static void pushZerosAtEnd(int[] arr) 
    {
        for(int i = 0, k = 0; i < arr.length; i++)
        {
            if(arr[i] != 0)
            {
                swap(i, k++, arr);
            }
        }
    }

    public static void swap(int i, int j, int[] arr)
    {
        int k = arr[i];
        arr[i] = arr[j];
        arr[j] = k;
    }
}
```
