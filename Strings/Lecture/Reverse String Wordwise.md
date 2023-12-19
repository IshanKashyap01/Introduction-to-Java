# Reverse String Wordwise

```Java
public class Solution 
{
    public static String reverseWordWise(String input) 
    {
        StringBuffer res = new StringBuffer();
        int j = 0;
        for(int i = 0; i < input.length(); i++)
        {
            if(input.charAt(i) == ' ')
            {
                res.insert(0, input.substring(j, i + 1));
                j = i + 1;
            }
        }
        res.insert(0, input.substring(j) + " ");
        return res.toString();
    }
}
```
