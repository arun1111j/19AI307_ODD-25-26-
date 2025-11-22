# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a Java program to implement a extending thread class


## AIM:
To implement multithreading in Java by extending the Thread class.


## ALGORITHM :
1.Create a class that extends Thread class
2.Override the run() method with thread execution logic
3.Create multiple thread objects in main method
4.Start threads using start() method
5.Observe concurrent execution





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Arun J
RegisterNumber: 212222040015
*/
```

## SOURCE CODE:
```
class MyThread extends Thread {
    private String threadName;
    
    // Constructor
    public MyThread(String name) {
        this.threadName = name;
    }
    
    // Override the run() method - this contains the code that will run in the thread
    @Override
    public void run() {
        try {
            // Simulate some work by making the thread sleep
            for (int i = 1; i <= 5; i++) {
                System.out.println("Thread: " + i + " from " + threadName);
                Thread.sleep(500); // Sleep for 500 milliseconds
            }
        } catch (InterruptedException e) {
            System.out.println("Thread " + threadName + " interrupted.");
        }
        System.out.println("Thread " + threadName + " finished.");
    }
}

public class Main {
    public static void main(String[] args) {
        System.out.println("Main thread started");
        
        // Create thread objects
        MyThread thread1 = new MyThread("Thread-1");
        MyThread thread2 = new MyThread("Thread-2");
        
        // Start the threads (this calls the run() method)
        thread1.start();
        thread2.start();
        
        // Main thread continues its own work
        try {
            // Wait for both threads to finish
            thread1.join();
            thread2.join();
        } catch (InterruptedException e) {
            System.out.println("Main thread interrupted.");
        }
        
        System.out.println("Main thread finished");
    }
}
```






## OUTPUT:
<img width="497" height="323" alt="image" src="https://github.com/user-attachments/assets/7c939dfb-f838-4e79-a81e-286daa853f1c" />


## RESULT:
Multithreading was successfully implemented by extending Thread class. Multiple threads executed concurrently, demonstrating proper thread creation and execution with separate call stacks.
