# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

## AIM:
To create a Car class with attributes brand, model, and year, and display details of two objects of the class.

## ALGORITHM :
1.Define a class named Car.
2.Declare three attributes: brand, model, and year.
3.Create a constructor to initialize these attributes.
4.Create a method to display the car details.
5.In the main method, create two objects of the Car class.
6.Print the details of both objects.





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Arun J
RegisterNumber:  212222040015
*/
```

## SOURCE CODE:
```
import java.util.*;
public class prog {
    public static void main(String[] args) {
        Car car1 = new Car();
        car1.brand = "Toyota";
        car1.model = "Innova";
        car1.year = 2022;

        Car car2 = new Car();
        car2.brand = "Hyundai";
        car2.model = "i20";
        car2.year = 2021;

        System.out.println("Car 1: " + car1.brand + " " + car1.model + " " + car1.year);
        System.out.println("Car 2: " + car2.brand + " " + car2.model + " " + car2.year);
    }
}
class Car
{
    public String brand;
    public String model;
    public int year;
}
```






## OUTPUT:

<img width="575" height="168" alt="image" src="https://github.com/user-attachments/assets/03a8666e-48bc-46e6-8014-a846a799b028" />


## RESULT:
The Car class was successfully implemented with attributes brand, model, and year. Two objects were created and their details were displayed correctly, confirming proper class functionality.
