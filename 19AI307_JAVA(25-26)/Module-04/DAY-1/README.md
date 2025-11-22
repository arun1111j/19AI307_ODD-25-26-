# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.


## AIM:
To read two integers and perform division with exception handling for division by zero.


## ALGORITHM :
1.Read two integers from user input
2.Use try-catch block to handle division operation
3.Perform division in try block
4.Catch ArithmeticException for division by zero case
5.Display result or error message accordingly




## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Arun J
RegisterNumber:  212222040015
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        int b = scanner.nextInt();
        
        try {
            if(b==0)
            {
                throw new ArithmeticException("Error: Division by zero");

            }
            System.out.println("Result: "+a / b);
        } catch (ArithmeticException e) {
            System.out.println(e.getMessage());
        }
        
        scanner.close();
    }
}
```






## OUTPUT:
<img width="646" height="281" alt="image" src="https://github.com/user-attachments/assets/08ac63e8-1499-4be0-af3b-ec7e9030f98f" />


## RESULT:
The program successfully handled division operations with proper exception handling. It correctly calculated division results for valid inputs and displayed appropriate error messages for division by zero cases.
