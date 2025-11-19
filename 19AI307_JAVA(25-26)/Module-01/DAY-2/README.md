# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
In a magical building, an elevator behaves oddly:
If the floor number is divisible by 3 and 5, it says "Skipped".
If the floor number is divisible by 3 only, it says "Beware!".
If the floor number is divisible by 5 only, it says "Blessings!".
Otherwise, it announces the floor number - print - "Floor {number}" .

Write a Java program to simulate this elevator logic for a given floor number.

## AIM:
To implement and verify the magical elevator announcement system using Java programming, demonstrating conditional logic based on divisibility rules.

## ALGORITHM :
1.START the program execution
2.CREATE Scanner object to read user input
3.READ integer floor number from user
4.APPLY conditional logic using modulus operator:
 If floor % 3 == 0 AND floor % 5 == 0 → Print "Skipped"
 Else if floor % 3 == 0 → Print "Beware!"
 Else if floor % 5 == 0 → Print "Blessings!"
 Else → Print "Floor " + floor
5.STOP the program execution

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Arun J
RegisterNumber:  212222040015
*/
```

## SOURCE CODE:

```
import java.util.*;
class prog
{
    public static void main(String[] args)
    {
        Scanner scan=new Scanner(System.in);
        int a=scan.nextInt();
        if(a%3==0 && a%5==0)
        {
            System.out.println("Skipped");
        }
        else if(a%3==0)
        {
            System.out.println("Beware!");
        }
        else if(a%5==0)
        {
            System.out.println("Blessings!");
        }
        else
        {
            System.out.println("Floor "+a);
        }
        
    }
}
```

## OUTPUT:

<img width="529" height="269" alt="image" src="https://github.com/user-attachments/assets/468ad6cb-3f62-4ee8-a533-c3ebfcd54e9a" />


## RESULT:
The Java program successfully implements the magical elevator logic and produces correct outputs for all test cases as per the given divisibility rules.

