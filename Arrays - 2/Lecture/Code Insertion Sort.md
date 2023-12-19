# Code Insertion Sort

```Java
public class Solution 
{
    public static void insertionSort(int[] arr, int size) 
    {
        for(int i = 1; i < size; i++)
        {
            for(int j = i; j > 0 && arr[j] < arr[j - 1]; j--)
            {
                swap(j, j - 1, arr);
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
