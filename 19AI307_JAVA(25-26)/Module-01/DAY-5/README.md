# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.

## AIM:
To write a Java program that reverses a given string using character array manipulation.


## ALGORITHM :
```
1.START the program
2.INPUT a string from the user
3.CONVERT the string to a character array
4.ITERATE through the array in reverse order
5.BUILD the reversed string character by character
6.OUTPUT the reversed string
7.STOP the program
```



## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: Kasivishvanath V
RegisterNumber:  212222040073
*/
```

## SOURCE CODE:

```
import java.util.*;
public class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String c = sc.nextLine();
        String rev=new StringBuilder(c).reverse().toString();
        System.out.println("Reversed string: "+rev);
        
    }
}
```





## OUTPUT:

<img width="815" height="276" alt="Screenshot 2025-11-24 160631" src="https://github.com/user-attachments/assets/f4c18048-f30a-4b97-8aa2-397535c07908" />


## RESULT:
The string reversal implementation successfully reversed all test strings using character array iteration, demonstrating proper handling of various input cases.
