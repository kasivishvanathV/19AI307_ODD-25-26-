# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Write a program to print "Hello, Ajeesh" using output statement.

## AIM:
To write, compile and execute a simple Java program that displays a message on the screen.

## ALGORITHM :
```
1. START the program
2. IMPORT Scanner class for reading input
3. CREATE a class named prog
4. DEFINE main() method
5. CREATE Scanner object to accept user input
6. READ the user’s name using Scanner
7. DISPLAY the message "Hello, [name]"
8. STOP the program

```

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Kasivishvanath V
RegisterNumber: 212222040073
*/
```

## Sourcecode.java:
```
import java.util.*;
class prog{
    
    public static void main(String args[])
    {
        Scanner sc=new Scanner(System.in);
        String name = sc.next();
        System.out.println("Hello, " + name);
    }
}
```


## OUTPUT:

<img width="736" height="169" alt="image" src="https://github.com/user-attachments/assets/353f359e-8c07-4e36-abc3-bcc19e5b5a70" />


## RESULT:
The Java program compiled and executed successfully, producing the output "Hello, Ajeesh", passing all test cases with a full score.





