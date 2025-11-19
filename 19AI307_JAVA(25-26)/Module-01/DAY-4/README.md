# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to Find the Average of Array Elements.

## AIM:
To write a Java program that calculates the average of elements in an array and verify its correctness with test cases.

## ALGORITHM :
```
1.START the program
2.DECLARE and INITIALIZE an array with numbers
3.CALCULATE sum of all array elements using loop
4.COMPUTE average by dividing sum by array length
5.DISPLAY the calculated average
6.STOP the program
```


## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
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
        double a=scan.nextDouble();
        double[] arr=new double[(int)a];
        double sum=0.0;
        for(int i=0;i<a;i++)
        {
            arr[i]=scan.nextDouble();
            sum+=arr[i];
        }
        double avg=sum/a;
        System.out.printf("The average of elements is %.2f",avg);
    }
}
```





## OUTPUT:

<img width="889" height="457" alt="image" src="https://github.com/user-attachments/assets/e548e4cf-1af5-4c1b-8e4b-fb33ddb7a7d6" />


## RESULT:
The array average implementation successfully calculated correct averages for all test cases using iterative summation and proper type casting.
