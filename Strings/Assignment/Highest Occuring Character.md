# Highest Occuring Character

```Java
public class Solution 
{
    public static char highestOccuringChar(String str) 
    {
        int[] freq = new int[256];
        for(int i = 0; i < str.length(); i++)
        {
            freq[str.charAt(i)]++;
        }
        int num = 0, index = 0;
        for(int i = 0; i < freq.length; i++)
        {
            index = num >= freq[i] ? index : i;
            num = Math.max(num, freq[i]);
        }
        return (char) index;
    }
}
```
