# Square Root (Integral)

```Java
import java.util.Scanner;

public class Main 
{    
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int i = 1, root = 0;
        while(i * i <= n)
        {
            root = i;
            if(i * i == n)
            {
                break;
            }
            i++;
        }
        System.out.println(root);
    }
}
```
