# Total Sum on the Boundaries and Diagonals

```Java
public class Solution 
{
    public static void totalSum(int[][] mat) 
    {
        int n = mat.length - 1, sum = 0;
        for(int i = 0, j = n; i <= n; i++, j--)
        {
            // columns
            sum += mat[i][0] + mat[i][n];
            if(i > 0 && i < n)
            {
                // rows
                sum += mat[0][i] + mat[n][i];
                // LR diagonal
                sum += mat[i][i];
                // RL diagonal
                sum += i == j ? 0 : mat[i][j];
            }
        }
        System.out.println(sum);
    }
}
```
