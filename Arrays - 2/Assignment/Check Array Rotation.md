# Check Array Rotation

```Java
public class Solution 
{
    public static int arrayRotateCheck(int[] arr)
    {
        int k = 0;
        for(int i = 0; i < arr.length - 1 && arr[i] > arr[arr.length - 1]; i++)
        {
            k++;
        }
        return k;
    }
}
```
