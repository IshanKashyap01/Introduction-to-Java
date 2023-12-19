# Remove Consecutive Duplicates

```Java
public class Solution 
{
    public static String removeConsecutiveDuplicates(String str) 
    {
        StringBuffer buff = new StringBuffer();
        buff.append(str.charAt(0));
        for(int i = 0; i < str.length(); i++)
        {
            if(str.charAt(i) != buff.charAt(buff.length() - 1))
            {
                buff.append(str.charAt(i));
            }
        }
        return buff.toString();
    }
}
```
