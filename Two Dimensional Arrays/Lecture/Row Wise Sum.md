# Row Wise Sum

```Java
public class Solution 
{
    public static void rowWiseSum(int[][] mat) 
    {
        int sum;
        for(int[] arr : mat)
        {
            sum = 0;
            for(int j : arr)
            {
                sum += j;
            }
            System.out.print(sum + " ");
        }
    }
}
```
