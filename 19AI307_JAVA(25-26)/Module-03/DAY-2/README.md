# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:


## AIM:
To implement method overloading by calculating area of different shapes using multiple methods with same name.

## ALGORITHM :
1.Create AreaCalculator class with overloaded area() methods
2.Implement methods for circle (radius), rectangle (length, breadth), and square (side)
3.Each method calculates and returns area based on parameters
4.In main method, test all overloaded methods with sample values





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Arun J
RegisterNumber:  212222040015
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class AreaCalculator {
    
    // Method to calculate area of square
    public int area(int side) {
        return side * side;
    }
    
    // Method to calculate area of rectangle
    public int area(int length, int breadth) {
        return length * breadth;
    }
    
    // Method to calculate area of circle
    public double area(double radius) {
        return Math.PI * radius * radius;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        AreaCalculator calculator = new AreaCalculator();
        
        // Read input for square
        int squareSide = scanner.nextInt();
        
        // Read input for rectangle
        int rectLength = scanner.nextInt();
        int rectBreadth = scanner.nextInt();
        
        // Read input for circle
        double circleRadius = scanner.nextDouble();
        
        // Calculate and display areas
        System.out.println("Area of square: " + calculator.area(squareSide));
        System.out.println("Area of rectangle: " + calculator.area(rectLength, rectBreadth));
        System.out.println("Area of circle: " + calculator.area(circleRadius));
        
        scanner.close();
    }
}
```






## OUTPUT:

<img width="738" height="336" alt="image" src="https://github.com/user-attachments/assets/5bc25180-87ee-4677-9067-dc9a63dfbabf" />



## RESULT:
Method overloading was successfully implemented. The AreaCalculator class correctly calculated areas for circle, rectangle, and square using same method name with different parameters, demonstrating compile-time polymorphism.
