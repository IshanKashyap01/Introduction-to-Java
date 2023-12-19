# Fahrenheit to Celsius Table

```Java
import java.util.Scanner;
public class Solution 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int s = sc.nextShort(), e = sc.nextShort(), w = sc.nextShort();
        for(int i = s; i <= e; i += w)
        {
            System.out.println(i + " " + toCelsius(i));
        }
    }

    public static int toCelsius(int far)
    {
        return (far - 32) * 5 / 9;
    }
}
```
