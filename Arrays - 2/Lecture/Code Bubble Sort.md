# Code Bubble Sort

```Java
public class Solution 
{
    public static void bubbleSort(int[] arr, int n) 
    {
        for(int i = 0; i < arr.length - 1; i++)
        {
            for(int j = 1; j < arr.length - i; j++)
            {
                if(arr[j] < arr[j - 1])
                {
                    swap(j, j - 1, arr);
                }
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
