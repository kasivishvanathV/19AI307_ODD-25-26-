# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.

Note : Read the threadname from the User

Set the Priority as 2.

## AIM:
To write a Java program that reads a thread name from the user, sets it as the name of the current thread, assigns priority 2, and displays the updated thread details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a scanner to read input from the user.
4.	Read a thread name from the user.
5.	Get the current thread using Thread.currentThread().
6.	Set the thread’s name using setName().
7.	Set the thread’s priority to 2 using setPriority(2).
8.	Display the thread’s name and priority.
9.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Kasivishvanath V
RegisterNumber: 212222040073 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ThreadPriorityNameExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();

        Thread currentThread = Thread.currentThread();

        currentThread.setName(threadName);
        currentThread.setPriority(2);

        System.out.println("Priority of Thread: " + currentThread.getPriority());
        System.out.println("Name of Thread: " + currentThread.getName());
        System.out.println(currentThread);

        sc.close();
    }
}

```
## OUTPUT:
<img width="714" height="222" alt="image" src="https://github.com/user-attachments/assets/39189942-25b0-41a8-a3ee-a7782a5e49cc" />



## RESULT:
When executed, the program successfully assigns the user-entered name to the current thread and sets its priority to 2.
