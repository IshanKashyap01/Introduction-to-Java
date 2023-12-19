# Print Spiral

```Java
public class Solution 
{
    public static void spiralPrint(int matrix[][])
    {
        if(matrix.length == 0)
        {
            return;
        }
        int elements = matrix.length * matrix[0].length;
        int rowStart = 0, rowEnd = matrix.length - 1;
        int colStart = 0, colEnd = matrix[0].length  - 1;

        while(elements > 0)
        {
            // Left to right
            for(int i = colStart; i <= colEnd && elements > 0; i++, elements--)
            {
                System.out.print(matrix[rowStart][i] + " ");
            }
            rowStart++;
            // Top right to bottom right
            for(int i = rowStart; i <= rowEnd && elements > 0; i++, elements--)
            {
                System.out.print(matrix[i][colEnd] + " ");
            }
            colEnd--;
            // Bottom right to bottom left
            for(int i = colEnd; i >= colStart && elements > 0; i--, elements--)
            {
                System.out.print(matrix[rowEnd][i] + " ");
            }
            rowEnd--;
            // Bottom left to top left
            for(int i = rowEnd; i >= rowStart && elements > 0; i--, elements--)
            {
                System.out.print(matrix[i][colStart] + " ");
            }
            colStart++;
        }
    }
}
```
