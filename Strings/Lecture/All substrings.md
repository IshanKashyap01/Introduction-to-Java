# All substrings

```Java
public class Solution 
{
    public static void printSubstrings(String str) 
    {
        for(int i = 0; i < str.length(); i++)
        {
            for(int j = i + 1; j <= str.length(); j++)
            {
                System.out.println(str.substring(i, j));
            }
        }
    }
}
```
