# Fahrenheit to Celsius Table

```Java
public class Solution 
{
    public static void printFahrenheitTable(int start, int end, int step) 
    {
        for(int i = start; i <= end; i += step)
        {
            System.out.println(i + " " + toCelsius(i));
        }
    }

    public static int toCelsius(int farhenheit)
    {
        return (int) (5 * (farhenheit - 32) / 9);
    }
}
```
