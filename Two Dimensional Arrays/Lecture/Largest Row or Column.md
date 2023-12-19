# Largest Row or Column

```Java
public class Solution 
{
    public static void findLargest(int mat[][])
    {
        int row = 0, rowSum = Integer.MIN_VALUE, temp = 0;
        for(int i = 0; i < mat.length; i++)
        {
            temp = getRowSum(mat[i]);
            if(temp > rowSum)
            {
                rowSum = temp;
                row = i;
            }
        }
        int colSum = Integer.MIN_VALUE, col = 0;
        for(int i = 0; mat.length > 0 && i < mat[0].length; i++)
        {
            temp = getColumnSum(mat, i);
            if(temp > colSum)
            {
                colSum = temp;
                col = i;
            }
        }
        if(rowSum < 0 && colSum < 0)
        {
            System.out.println("row 0 " + rowSum);
        }
        else
        {
            if(rowSum == colSum)
            {
                if(row >= col)
                {
                    System.out.println("row " + row + " " + rowSum);
                }
                else
                {
                    System.out.println("column " + col + " " + colSum);
                }
            }
            else if(rowSum > colSum)
            {
                System.out.println("row " + row + " " + rowSum);
            }
            else
            {
                System.out.println("column " + col + " " + colSum);
            }
        }
    }

    public static int getRowSum(int[] arr)
    {
        int sum = 0;
        for(int i : arr)
        {
            sum += i;
        }
        return sum;
    }

    public static int getColumnSum(int[][] mat, int col)
    {
        int sum = 0;
        for(int i = 0; i < mat.length; i++)
        {
            sum += mat[i][col];
        }
        return sum;
    }
}
```
