# Check Number sequence

```Java
import java.util.Scanner;

public class Main 
{    
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(), prev = sc.nextInt(), curr;
        int i = 1;
        boolean isDec = true;
        while(i < n)
        {
            curr = sc.nextInt();
            i++;
            if(prev == curr)
            {
                System.out.println(false);
                return;
            }
            else if(curr < prev)
            {
                if(!isDec)
                {
                    System.out.println(false);
                    return;
                }
            }
            else
            {
                isDec = false;
            }
            prev = curr;
        }
        System.out.println(true);
    }
}
```
