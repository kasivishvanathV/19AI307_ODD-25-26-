# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

## AIM:
To create a Car class with attributes brand, model, and year, and display details of two objects of the class.

## ALGORITHM :
1.Define a class named Car.
2.Declare three attributes: brand, model, and year.
3.Create a constructor to initialize these attributes.
4.Create a method to display the car details.
5.In the main method, create two objects of the Car class.
6.Print the details of both objects.





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Arun J
RegisterNumber:  212222040015
*/
```

## SOURCE CODE:
```
class Car {
    String brand;
    String model;
    int year;
    Car(String brand, String model, int year) {
        this.brand = brand;
        this.model = model;
        this.year = year;
    }
    void displayDetails(String carName) {
        System.out.println(carName + ": " + brand + " " + model + " " + year);
    }
}

public class Main {
    public static void main(String[] args) {
        Car car1 = new Car("Toyota", "Innova", 2022);
        Car car2 = new Car("Hyundai", "i20", 2021);
        car1.displayDetails("Car 1");
        car2.displayDetails("Car 2");
    }
}

```






## OUTPUT:

<img width="717" height="205" alt="Screenshot 2025-11-24 161214" src="https://github.com/user-attachments/assets/cfbffd96-8b80-4739-94a5-e5043ddd549f" />



## RESULT:
The Car class was successfully implemented with attributes brand, model, and year. Two objects were created and their details were displayed correctly, confirming proper class functionality.
