# Reverse Each Word

```Java
public class Solution 
{
    public static String reverseEachWord(String str) 
    {
        StringBuffer buff = new StringBuffer();
        int j = 0;
        for(int i = 0; i < str.length(); i++)
        {
            if(str.charAt(i) == ' ')
            {
                buff.append(reverse(str.substring(j, i)) + " ");
                j = i + 1;
            }
        }
        buff.append(reverse(str.substring(j)));
        return buff.toString();
    }

    public static String reverse(String word)
    {
        return new StringBuffer(word).reverse().toString();
    }
}
```
