# Minimum Length Word

```Java
public class Solution 
{    
    public static String minLengthWord(String input)
    {
        String[] words = input.split(" ");
        String min = words[0];
        for(String word : words)
        {
            min = min.length() <= word.length() ? min : word;
        }
        return min;
    }
}
```
