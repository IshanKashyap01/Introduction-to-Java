# Print Like a Wave

```Java
public class Solution 
{
    public static void wavePrint(int mat[][])
    {
        if(mat.length == 0)
        {
            return;
        }
        boolean bool = true;
        for(int j = 0; j < mat[0].length; j++)
        {
            bool = bool ? print(mat, j) : printReverse(mat, j);
        }
    }

    private static boolean print(int[][] mat, int col)
    {
        for(int i = 0; i < mat.length; i++)
        {
            System.out.print(mat[i][col] + " ");
        }
        return false;
    }

    private static boolean printReverse(int[][] mat, int col)
    {
        for(int i = mat.length - 1; i >= 0; i--)
        {
            System.out.print(mat[i][col] + " ");
        }
        return true;
    }
}
```
