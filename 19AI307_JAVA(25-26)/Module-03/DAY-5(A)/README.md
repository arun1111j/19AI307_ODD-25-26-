# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.


## AIM:
To check if a user-input number is an Armstrong number using Math.pow() and Integer wrapper class.

## ALGORITHM :
1.Take integer input from user using Scanner
2.Convert number to string to get digits using Integer and String methods
3.Calculate sum of each digit raised to power of digit count using Math.pow()
4.Compare sum with original number to determine Armstrong number
5.Display the result




## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Arun J
RegisterNumber:  212222040015
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ArmstrongCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();

        String numStr = Integer.toString(num);
        int length = numStr.length();
        int sum = 0, temp = num;

        while (temp > 0) {
            int digit = temp % 10;
            sum += (int) Math.pow(digit, length);
            temp /= 10;
        }

        if (sum == num) {
            System.out.println(num + " is an Armstrong number.");
        } else {
            System.out.println(num + " is not an Armstrong number.");
        }

        sc.close();
    }
}
```






## OUTPUT:
<img width="717" height="228" alt="image" src="https://github.com/user-attachments/assets/1bf9e194-6be4-417e-ad41-b28738c7d797" />



## RESULT:
The program successfully identified Armstrong numbers. It correctly calculated the sum of digits raised to appropriate power and accurately determined whether input numbers were Armstrong numbers or not.
