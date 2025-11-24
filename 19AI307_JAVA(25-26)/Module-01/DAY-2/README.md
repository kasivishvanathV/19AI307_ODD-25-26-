# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
A pirate ship has a code lock that only opens if:

The input code is even, and

If it is less than 100, say "Weak Code".

If it is between 100 and 999, say "Strong Code".

If the code is odd, deny access.

## AIM:
To classify a pirate code as Weak, Strong, or Denied.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the input code from the user.
4.	Check if the code is odd — if true, print "Access Denied".
5.	If the code is even and less than 100, print "Weak Code".
6.	If the code is even and between 100 and 999, print "Strong Code".
7.	End the program.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Kasivishvanath V
RegisterNumber: 212222040073 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class PirateCodeLock {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int code = sc.nextInt();

        if (code % 2 != 0) {
            System.out.println("Access Denied");
        } else {
            if (code < 100) {
                System.out.println("Weak Code");
            } else if (code >= 100 && code <= 999) {
                System.out.println("Strong Code");
            } else {
                System.out.println("Access Denied"); 
            }
        }

        sc.close();
    }
}

```
## OUTPUT:
<img width="572" height="374" alt="image" src="https://github.com/user-attachments/assets/dae2b989-f163-41dc-8624-39338702af66" />


## RESULT:
Thus, the Java program successfully checks the pirate code and displays whether it is a Weak Code, Strong Code, or Access Denied.

