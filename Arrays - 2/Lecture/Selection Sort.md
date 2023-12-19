# Selection Sort

```Java
public class Solution 
{
    public static void selectionSort(int[] arr) 
    {
        int min, index = 0;
        for(int i = 0; i < arr.length - 1; i++)
        {
            min = Integer.MAX_VALUE;
            for(int j = i; j < arr.length; j++)
            {
                index = arr[j] < min ? j : index;
                min = arr[index];
            }
            swap(i, index, arr);
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
