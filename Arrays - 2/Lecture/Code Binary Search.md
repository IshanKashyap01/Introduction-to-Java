# Code Binary Search

```Java
public class Solution 
{
    public static int search(int []nums, int target) 
    {
        int i = 0, j = nums.length - 1, mid;
        while(i <= j)
        {
            mid = (i + j) / 2;
            if(target == nums[mid])
            {
                return mid;
            }
            if(target < nums[mid])
            {
                j = mid - 1;
            }
            else
            {
                i = mid + 1;
            }
        }
        return -1;
    }
}
```
