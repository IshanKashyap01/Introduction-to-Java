# Second Largest in array

```Java
public class Solution 
{  
    public static int secondLargestElement(int[] arr, int n) 
    {
        int largest = Integer.MIN_VALUE, second = Integer.MIN_VALUE;
        for(int i = 0; i < arr.length; i++)
        {
            if(arr[i] > largest)
            {
                second = largest;
                largest = arr[i];
            }
            else if(arr[i] > second)
            {
                second = arr[i];
            }
        }
        return second;
    }
}
```
