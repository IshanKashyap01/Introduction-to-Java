# Remove character

```Java
public class Solution 
{
    public static String removeAllOccurrencesOfChar(String str, char ch) 
    {
        StringBuffer buff = new StringBuffer();
        for(int i = 0; i < str.length(); i++)        
        {
            if(str.charAt(i) != ch)
            {
                buff.append(str.charAt(i));
            }
        }
        return buff.toString();
    }
}
```
