# Compress the String

```Java
public class Solution 
{
    public static String getCompressedString(String str) 
    {
        StringBuffer buff = new StringBuffer();
        buff.append(str.charAt(0));
        int num = 1;
        for(int i = 1; i < str.length(); i++)
        {
            if(str.charAt(i) == buff.charAt(buff.length() - 1))
            {
                num++;
            }
            else
            {
                buff.append(num > 1 ? num : "");
                buff.append(str.charAt(i));
                num = 1;
            }
        }
        buff.append(num > 1 ? num : "");
        return buff.toString();
    }
}
```
