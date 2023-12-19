# Sort 0 1

```Java
public class Solution 
{  
    public static void sortZeroesAndOne(int[] arr) 
    {
        int i = 0, j = arr.length - 1;
        while(i < j)
        {
           if(arr[i] == 1 && arr[j] == 0)
           {
               arr[i] = 0;
               arr[j] = 1;
           }
           else if(arr[i] == 0)
           {
               i++;
           }
           else
           {
               j--;
           }
        }
    }
}
```
