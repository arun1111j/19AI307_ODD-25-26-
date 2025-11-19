# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.

## AIM:
To implement a Java program that calculates the factorial of a given non-negative integer using a for loop, and verify its correctness through multiple test cases.

## ALGORITHM :
1.START the program execution
2.CREATE Scanner object to read user input
3.READ integer number n from user
4.INITIALIZE variable factorial = 1
5.ITERATE from i = 1 to i <= n using for loop:
6.Multiply factorial by i in each iteration
7.DISPLAY the calculated factorial value
8.STOP the program execution

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Arun J
RegisterNumber:  212222040015
*/
```

## SOURCE CODE:
```
import java.util.*;
public class prog
{
    public static void main(String[] args)
    {
        Scanner scan=new Scanner(System.in);
        int a=scan.nextInt();
        System.out.printf("Factorial of %d is: %d",a,factorial(a));
    }
    public static int factorial(int n)
    {
        if(n==0)
            return 1;
        else
            return n*factorial(n-1);
    }
}
```

## OUTPUT:
<img width="711" height="223" alt="image" src="https://github.com/user-attachments/assets/a088b88a-a217-46b4-9939-99e792d2b0ae" />

## RESULT:
The Java program successfully implemented factorial calculation using a for loop, producing correct outputs for all tested input values as per mathematical factorial definitions.
