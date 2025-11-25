# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

finalPrice = purchaseWeight * (goldRatePerGram - discount)

For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).

## AIM:
To write a Java program that uses inheritance to calculate the final price paid by Regular and Premium customers based on gold rate per gram, discount rules, and cashback.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a base class Customer with attributes customerId, name, and purchaseWeight.
4.	Create derived classes RegularCustomer and PremiumCustomer that apply their respective discounts and compute the final price.
5.	In the main method, input the gold rate per gram, create customer objects, calculate their final price (and cashback for premium), and display the results.

## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Kasivishvanath V
RegisterNumber: 212222040073 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmountPerGram = goldRatePerGram * getDiscountRate() / 100.0;
        double effectiveRate = goldRatePerGram - discountAmountPerGram;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + String.format("%.1f", purchaseWeight) + " grams");
        System.out.println("Gold Rate per Gram: " + String.format("%.1f", goldRatePerGram));
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + String.format("%.2f", calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 2;
    }

    void display() {
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + String.format("%.1f", purchaseWeight) + " grams");
        System.out.println("Gold Rate per Gram: " + String.format("%.1f", goldRatePerGram));
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + String.format("%.2f", calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 5;
    }

    double cashback() {
        return calculateFinalPrice() * 0.01;
    }

    void display() {
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + String.format("%.1f", purchaseWeight) + " grams");
        System.out.println("Gold Rate per Gram: " + String.format("%.1f", goldRatePerGram));
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + String.format("%.2f", calculateFinalPrice()));
        System.out.println("Cashback: " + String.format("%.2f", cashback()));
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String type = sc.nextLine().trim();
        String id = sc.nextLine().trim();
        String name = sc.nextLine().trim();
        double weight = Double.parseDouble(sc.nextLine().trim());
        double rate = Double.parseDouble(sc.nextLine().trim());
        Customer customer;
        if (type.equalsIgnoreCase("Regular")) {
            customer = new RegularCustomer(id, name, weight, rate);
        } else if (type.equalsIgnoreCase("Premium")) {
            customer = new PremiumCustomer(id, name, weight, rate);
        } else {
            customer = new Customer(id, name, weight, rate);
        }
        customer.display();
        sc.close();
    }
}


```
## OUTPUT:
<img width="904" height="808" alt="image" src="https://github.com/user-attachments/assets/411c0831-0c3e-4764-91b7-5cbc3878f63f" />



## RESULT:
The program successfully calculates:

Final price for the RegularCustomer with a 2% discount.

Final price for the PremiumCustomer with a 5% discount.

Cashback amount (1% of final price) for the premium customer.
