# Print 2D Array

```Java
public class Solution 
{
    public static void print2DArray(int input[][]) 
    {
        for(int i = 0; i < input.length; i++)
        {
            for(int j = i; j < input.length; j++)
            {
                print(input[i]);
            }
        }
    }

    public static void print(int[] arr)
    {
        for(int i : arr)
        {
            System.out.print(i + " ");
        }
        System.out.println();
    }
}
```
