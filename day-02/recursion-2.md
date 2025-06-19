# Recursion

### Reversing a number - (Iterative approach)

```java
import java.util.Scanner;
public class ReverseNumber{
  public static int reverseNumber(int num){
    int rev = 0;
    while(num >0){
      int lastDigit = num % 10; 
      rev = rev*10 + lastDigit;
      num /=10;
    }
    return rev;
  }
  public static void main(String args[]){
    Scanner sc = new Scanner(System.in);
    System.out.print("Enter a number (to be reversed): ");
    int x = sc.nextInt();
    int rev = reverseNumber(x);
    System.out.print("The reverse of "+ x +" is "+ rev);
  }
}

```


### Reversing a number - (Recursive approach) 


```java
import java.util.Scanner;
public class ReverseNumber{
  public static int reverseNumber(int num, int rev){
   if(num == 0){
       return rev;
   }
   int lastDigit = num % 10;
   rev = rev*10 + lastDigit;
   return reverseNumber(num/10, rev);
  }
  public static void main(String args[]){
    Scanner sc = new Scanner(System.in);
    System.out.print("Enter a number (to be reversed): ");
    int x = sc.nextInt();
    int rev = reverseNumber(x, 0);
    System.out.print("The reverse of "+ x +" is "+ rev);
  }
}
```

**Sample Output:**

```bash
Enter a number (to be reversed): 523
The reverse of 523 is 325
```

### Armstrong number - (Iterative Approach)

```java

import java.util.Scanner;
import java.lang.Math;
import java.lang.String;

public class ArmstrongNumber{
  public static boolean checkArmstrong(int num){
    int num1 = num;
    int n = num.toString().length();
    int sum = 0;
    while(num > 0){
      int rem = num % 10;
      sum = math.pow(rem, n);
      num /= 10;
    }
    return num1 == sum ? true : false; 
  }
  public static void main(String args[]){
    Scanner sc = new Scanner(System.in);
    System.out.print("Enter a number: ");
    int num = sc.nextInt();
    boolean isArmstrong = checkArmstrong(num);
    if(isArmstrong){
      System.out.println(num + " is an Armstrong number");
    }else{
      System.out.println(num + " is not an Armstrong number");
    }
  }
}

```

