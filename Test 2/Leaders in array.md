# Leaders in array

```Java
public class Solution 
{
    public static void leaders(int[] input) 
    {
        for(int i = 0; i < input.length; i++)
        {
            if(isLeader(i, input))
            {
                System.out.print(input[i] + " ");
            }
        }
    }

    private static boolean isLeader(int i, int[] input)
    {
        for(int j = i + 1; j < input.length; j++)
        {
            if(input[j] > input[i])
            {
                return false;
            }
        }
        return true;
    }
}
```
