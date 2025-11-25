# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program where the inner class is declared private and accessed through a method in the outer class. 

Input	Result
3
Data set inside private inner class: 3


## AIM:
To demonstrate how a private inner class can be accessed from outside via an outer class method.

## ALGORITHM :
1. Create an outer class Outer.
2. Declare a private inner class Inner with a variable and a method to display data.
3. In Outer, create a method createInner(int x) that:
       - Creates an Inner object
       - Sets its data
       - Calls its display method
4. In main():
       - Read an integer
       - Create Outer object
       - Call createInner() with the input.





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Kasivishvanath V
RegisterNumber: 212222040073
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Outer {

    private class Inner {
        int data;

        void show() {
            System.out.println("Data set inside private inner class: " + data);
        }
    }

    void createInner(int x) {
        Inner obj = new Inner();
        obj.data = x;
        obj.show();
    }
}

class Sourcecode {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        Outer outer = new Outer();
        outer.createInner(n);
    }
}
```

## OUTPUT:
<img width="439" height="118" alt="image" src="https://github.com/user-attachments/assets/8ba5a2cd-6537-491f-8665-f503896331f2" />



## RESULT:
The private inner class is successfully accessed through an outer class method.
