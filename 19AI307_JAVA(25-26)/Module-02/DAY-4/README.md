# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Implement a class Employee with a parameterized constructor to initialize id, name, and salary.

## AIM:
To write a Java program that demonstrates variable scope and constructors by initializing employee details through a parameterized constructor.

## ALGORITHM :
1. Start the program.
2. Import the java.util package.
3. Create a class Employee with instance variables id, name, and salary.
4. Define a parameterized constructor to initialize these variables.
5. In the main method, create a Scanner object to read input values.
6. Read id, name, and salary from the user.
7. Create an object of Employee using the parameterized constructor.
8. Access and display the initialized values.
9. End the program.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Kasivishvanath V
RegisterNumber: 212222040073
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class Employee {
    private int id;
    private String name;
    private double salary;

    Employee(int id, String name, double salary) {
        this.id = id;
        this.name = name;
        this.salary = salary;
    }

    void display() {
        System.out.println("Employee Details:");
        System.out.println("Employee ID: " + id);
        System.out.println("Employee Name: " + name);
        System.out.println("Employee Salary: " + salary);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int id = sc.nextInt();
        sc.nextLine();
        String name = sc.nextLine();
        double salary = sc.nextDouble();
        Employee emp = new Employee(id, name, salary);
        emp.display();
        sc.close();
    }
}

```

## OUTPUT:

<img width="878" height="540" alt="image" src="https://github.com/user-attachments/assets/3dca16b9-716b-4385-97cc-2df42294d1f2" />


## RESULT:
  Thus, the Java program was successfully written and executed using a parameterized constructor to initialize employee details.

