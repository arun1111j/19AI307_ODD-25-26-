# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a Java program to create a new file named example.txt.


## AIM:
To create a new file named example.txt using Java file handling.


## ALGORITHM :
1.Import java.io package
2.Create File object with filename "example.txt"
3.Use createNewFile() method to create the file
4.Check return value to confirm successful creation
5.Handle IOException if file creation fails





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Arun J
RegisterNumber:  212222040015
*/
```

## SOURCE CODE:
```
import java.io.File;
import java.io.IOException;

public class CreateFileExample {
    public static void main(String[] args) {
        File file = new File("example.txt");
        
        try {
            if (file.createNewFile()) {
                System.out.println("File created: example.txt");
            } else {
                System.out.println("File already exists: example.txt");
            }
        } catch (IOException e) {
            System.out.println("An error occurred: " + e.getMessage());
        }
    }
}
```




## OUTPUT:
<img width="674" height="207" alt="image" src="https://github.com/user-attachments/assets/da5e7370-91a6-45ef-bd7b-4ea3b541d8e5" />


## RESULT:
The program successfully created a new file named example.txt. File creation was verified and proper exception handling was implemented for IO operations.
