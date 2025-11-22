# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks:

## AIM:
To implement inheritance by creating a Person superclass and Student subclass with grade calculation functionality.

## ALGORITHM :
1.Create Person class with name and age fields
2.Create Student class that extends Person and adds marks field
3.Implement calculateGrade() method in Student that returns grade based on marks
4.In main method, create Student object and test grade calculation





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Arun j
RegisterNumber:  212222040015
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Person {
    String name;
    int age;
}

class Student extends Person {
    int marks;
    
    String calculateGrade() {
        if (marks >= 90) {
            return "A";
        } else if (marks >= 75) {
            return "B";
        } else if (marks >= 50) {
            return "C";
        } else {
            return "F";
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        Student s = new Student();
        
        System.out.print("Name: ");
        s.name = scan.next();
        System.out.println(s.name);
        System.out.print("Age: ");
        s.age = scan.nextInt();
        System.out.println(s.age);

        System.out.print("Marks: ");
        s.marks = scan.nextInt();
        System.out.println(s.marks);

        System.out.println("Grade: " + s.calculateGrade());
    }
}
```






## OUTPUT:

<img width="530" height="550" alt="image" src="https://github.com/user-attachments/assets/7e50b312-7057-4271-b9e7-472ef8cc608f" />



## RESULT:
The inheritance hierarchy was successfully implemented. The Student class inherited name and age from Person class and correctly calculated grades based on marks, demonstrating proper inheritance and method implementation.
