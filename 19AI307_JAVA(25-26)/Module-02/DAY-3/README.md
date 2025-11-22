# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.



## AIM:
To create a Smartphone class with private variables and implement getter/setter methods along with an increaseStorage() method.

## ALGORITHM :
1.Create Smartphone class with private variables: brand, model, storageCapacity
2.Implement public getter and setter methods for all variables
3.Create increaseStorage() method that takes integer and adds to storageCapacity
4.In main method, create Smartphone object and test all methods





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Arun J
RegisterNumber:  212222040015
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Smartphone {
    private String brand;
    private String model;
    private int storageCapacity;

    public String getBrand() {
        return brand;
    }

    public String getModel() {
        return model;
    }

    public int getStorageCapacity() {
        return storageCapacity;
    }

    public void setBrand(String brand) {
        this.brand = brand;
    }

    public void setModel(String model) {
        this.model = model;
    }

    public void setStorageCapacity(int storageCapacity) {
        this.storageCapacity = storageCapacity;
    }

    public void increaseStorage(int value) {
        if (value > 0) {
            this.storageCapacity += value;
        }
    }

    public void display() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
        System.out.println("------------------------------");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        Smartphone phone = new Smartphone();
        
        String brand = scanner.nextLine();
        String model = scanner.nextLine();
        int storage = scanner.nextInt();
        int increaseValue = scanner.nextInt();
        
        phone.setBrand(brand);
        phone.setModel(model);
        phone.setStorageCapacity(storage);

        phone.increaseStorage(increaseValue);
        
        phone.display();
        
        scanner.close();
    }
}
```






## OUTPUT:
<img width="852" height="394" alt="image" src="https://github.com/user-attachments/assets/26065bb6-f3ce-461c-9a08-4f4bb692f41e" />



## RESULT:
 The Smartphone class implementation was successful. All private variables, getter/setter methods, and the increaseStorage() function work correctly as verified through testing.
