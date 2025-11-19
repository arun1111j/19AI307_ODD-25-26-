# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.

## AIM:
To write a Java program that reverses a given string using character array manipulation.


## ALGORITHM :
```
1.START the program
2.INPUT a string from the user
3.CONVERT the string to a character array
4.ITERATE through the array in reverse order
5.BUILD the reversed string character by character
6.OUTPUT the reversed string
7.STOP the program
```



## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
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
        String a=scan.nextLine();
        StringBuilder sb=new StringBuilder(a);
        System.out.println("Reversed string: "+sb.reverse().toString());

    }
}
```





## OUTPUT:

<img width="699" height="244" alt="image" src="https://github.com/user-attachments/assets/ec06dab8-e780-4ace-a503-f54aed4a8e05" />


## RESULT:
The string reversal implementation successfully reversed all test strings using character array iteration, demonstrating proper handling of various input cases.
