# Check Permutation

```Java
public class Solution 
{
    public static boolean isPermutation(String str1, String str2) 
    {
        if(str1.length() != str2.length())
        {
            return false;
        }
        int check = 0;
        for(int i = 0; i < str1.length(); i++)
        {
            check ^= str1.charAt(i) ^ str2.charAt(i);
        }
        return check == 0;
    }
}
```
