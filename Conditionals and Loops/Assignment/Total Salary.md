# Total Salary

```Java
import java.util.Scanner;
public class Solution
{
    public static void main(String[] args) 
    {
        //Write your code here.
        Scanner sc = new Scanner(System.in);
        int basic = sc.nextInt();
        char grade = sc.next().charAt(0);
        double sal = 1.59 * basic;
        switch(grade)
        {
            case 'A' : sal += 1700; break;
            case 'B' : sal += 1500; break;
            default : sal += 1300;
        }
        System.out.print(Math.round(sal));
    }
}
```
