# Sum of Two Arrays

```Java
public class Solution 
{
    public static void sumOfTwoArrays(int arr1[], int arr2[], int output[]) 
    {
        int[] small = arr1.length < arr2.length ? arr1 : arr2;
        int[] big = small == arr2 ? arr1 : arr2;

        int carry = 0;
        int i = big.length - 1, j = small.length - 1, k = output.length - 1;
        while(j >= 0)
        {
            output[k--] = (big[i] + small[j] + carry) % 10;
            carry = (big[i--] + small[j--] + carry) / 10;
        }
        while(i >= 0)
        {
            output[k--] = (big[i] + carry) % 10;
            carry = (big[i--] + carry) / 10;
        }
        output[0] = carry;
    }
}
```
