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

<img width="1285" height="261" alt="Screenshot 2025-11-24 151927" src="https://github.com/user-attachments/assets/ab9ab05b-ced3-4d09-a8e5-8d4fcf826a32" />


## RESULT:
The Java program compiled and executed successfully, producing the output "Hello, Ajeesh", passing all test cases with a full score.






