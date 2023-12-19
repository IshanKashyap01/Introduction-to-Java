# Sort 0 1 2

```Java
public class Solution 
{
    public static void sort012(int[] arr)
    {
        int zero = 0, two = arr.length - 1, i = 0;
        while(i <= two)
        {
            if(arr[i] == 0)
            {
                swap(i++, zero++, arr);
            }
            else if(arr[i] == 2)
            {
                swap(i, two--, arr);
            }
            else
            {
                i++;
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
