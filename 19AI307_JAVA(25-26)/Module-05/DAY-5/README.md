# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Create a program that reads a thread name and a priority (1–10), sets that priority to a new thread, prints both values.


## AIM:
To create a thread with user-defined name and priority, then display both values.


## ALGORITHM :
1.Read thread name and priority (1-10) from user input
2.Create a new Thread with the given name
3.Set thread priority using setPriority() method
4.Start the thread and print name and priority values
5.Verify priority setting within valid range





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
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
        
        String threadName = scanner.nextLine();
        
        int priority = scanner.nextInt();
        
        Thread userThread = new Thread(threadName);
        
        userThread.setPriority(priority);
        
        System.out.println("Thread " + userThread.getName() + " priority is " + userThread.getPriority());
        
        scanner.close();
    }
}
```






## OUTPUT:
<img width="772" height="356" alt="image" src="https://github.com/user-attachments/assets/68be5516-b0d9-4b15-a9c5-8922fc14898a" />



## RESULT:
The program successfully created threads with user-specified names and priorities. Both thread name and priority values were correctly set and displayed, demonstrating proper thread configuration.
