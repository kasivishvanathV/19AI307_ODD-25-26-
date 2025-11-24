# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to print the Fibonacci series using a for loop. The series starts with 0 and 1, and the next number is the sum of the previous two.

## AIM:
To write a Java program that prints the Fibonacci series using a for loop.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to read the number of Fibonacci terms from the user.
4.	Initialize the first two Fibonacci numbers (a = 0, b = 1) and print them.
5.	Use a for loop to calculate and print the remaining Fibonacci numbers by adding the previous two.
6.	End the program.
   
## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Kasivishvanath V
RegisterNumber: 212222040073 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class FibonacciSeries {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int first = 0, second = 1;
        System.out.print("Fibonacci Series: ");
        System.out.print(first + " " + second);
        for (int i = 3; i <= n; i++) {
            int next = first + second;
            System.out.print(" " + next);
            first = second;
            second = next;
        }
    }
}

```
## OUTPUT:

<img width="815" height="333" alt="Screenshot 2025-11-24 155323" src="https://github.com/user-attachments/assets/84db2286-dcd2-44b2-a468-414e133ef26a" />



## RESULT:
Thus, the Java program successfully prints the Fibonacci series using a for loop.
