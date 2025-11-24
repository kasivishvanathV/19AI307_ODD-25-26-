# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the sum of even and odd elements in an array

## AIM:
To write a Java program to find the sum of even and odd elements in an array.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Initialize two variables: evenSum = 0 and oddSum = 0.
4.	Traverse the array using a loop and add each element to its respective sum based on whether it is even or odd.
5.	Print the sum of even elements and the sum of odd elements, then end the program.

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: Kasivishvanath V
RegisterNumber: 212222040073 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class SumEvenOdd {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        int sumEven = 0;
        int sumOdd = 0;
        for (int i = 0; i < n; i++) {
            if (arr[i] % 2 == 0) {
                sumEven += arr[i];
            } else {
                sumOdd += arr[i];
            }
        }
        System.out.println("Sum of even elements: " + sumEven);
        System.out.println("Sum of odd elements: " + sumOdd);
        sc.close();
    }
}
```

## OUTPUT:
<img width="810" height="690" alt="Screenshot 2025-11-24 160018" src="https://github.com/user-attachments/assets/1913a5fb-d5bd-4c57-b7b6-92e3660f02ee" />




## RESULT:
Thus, the Java program successfully calculates and displays the sum of even and odd elements in an array.
