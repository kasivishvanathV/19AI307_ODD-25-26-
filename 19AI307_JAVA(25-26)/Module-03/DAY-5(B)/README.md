# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to convert a string to an integer using a wrapper class and perform addition.

## AIM:
To write a Java program that converts a string to an integer using a wrapper class and performs addition.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a numeric string from the user.
4.	Convert the string to an integer using the Integer wrapper class (Integer.parseInt()).
5.	Add the integer to another number and display the result.
## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Kasivishvanath V
RegisterNumber: 212222040073  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class StringToIntAddition {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num1 = Integer.parseInt(sc.next());
        int num2 = Integer.parseInt(sc.next());

        System.out.println("Sum = " + (num1 + num2));
    }
}

```

## OUTPUT:
<img width="433" height="426" alt="image" src="https://github.com/user-attachments/assets/a0d6bc02-4e11-440f-9db6-347ad3b21db4" />



## RESULT:
The program successfully converts a string into an integer using the Integer wrapper class and performs addition, displaying the correct final result.

