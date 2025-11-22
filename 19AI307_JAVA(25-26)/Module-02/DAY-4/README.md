# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program to access a static variable using both class name and object.



## AIM:
To demonstrate accessing a static variable using both class name and object reference.


## ALGORITHM :
1.Create a class with a static variable
2.Access the static variable directly using class name
3.Create an object and access the static variable using object reference
4.Display the values to verify both access methods work




## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Arun J
RegisterNumber:  212222040015
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class StaticAccess {
    static int value;

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        value = sc.nextInt();

        System.out.println("Accessing using class name: " + StaticAccess.value);

        StaticAccess obj = new StaticAccess();
        System.out.println("Accessing using object: " + obj.value);

        sc.close();
    }
}
```







## OUTPUT:

<img width="713" height="261" alt="image" src="https://github.com/user-attachments/assets/be72ada1-1c10-4693-9cf2-19fc3a05bc44" />



## RESULT:
The program successfully demonstrated that static variables can be accessed using both class name and object reference. Both access methods returned the same value, confirming static variables belong to the class rather than individual objects.

