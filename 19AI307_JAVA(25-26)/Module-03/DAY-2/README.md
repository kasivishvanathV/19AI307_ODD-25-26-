# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program demonstrating method overriding. Create a class Animal with a method sound(). Subclass it as Dog, Cat, Cow, each overriding the sound() method.

## AIM:
To write a Java program that demonstrates runtime polymorphism by creating a superclass Animal and subclasses Dog, Cat, and Cow, each overriding the sound() method. The program should accept an animal name as input and print the corresponding sound.

## ALGORITHM :
1.Start the program.
2.Create a superclass Animal with a method sound().
3.Create subclasses Dog, Cat, and Cow that override the sound() method with specific outputs.
4.In the main() method, read a string input from the user.
5.Convert the input to lowercase and match it using a switch statement.
6.Based on the input:
   * If input is "dog", create a Dog object.
   * If input is "cat", create a Cat object.
   * If input is "cow", create a Cow object.
   * Otherwise, print "Unknown animal" and exit.
7.Call the sound() method through the superclass reference to demonstrate polymorphism.
8.End the program.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Kasivishvanath V
RegisterNumber:  212222040073
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Animal {
    public void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    public void sound() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    public void sound() {
        System.out.println("Cat meows");
    }
}

class Cow extends Animal {
    public void sound() {
        System.out.println("Cow moos");
    }
}

public class AnimalSound {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Animal a;

        String input = scanner.nextLine().trim().toLowerCase();

        switch (input) {
            case "dog":
                a = new Dog();
                break;
            case "cat":
                a = new Cat();
                break;
            case "cow":
                a = new Cow();
                break;
            default:
                System.out.println("Unknown animal");
                scanner.close();
                return;
        }

        a.sound();
        scanner.close();
    }
}

```

## OUTPUT:

<img width="879" height="412" alt="Screenshot 2025-11-25 120201" src="https://github.com/user-attachments/assets/1986bed4-c369-49ee-84c0-c8f8a0894871" />


## RESULT:
The Java program was executed successfully.When an animal name was entered, the program displayed the correct sound by calling the overridden sound() method using runtime polymorphism.
