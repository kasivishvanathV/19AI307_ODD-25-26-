# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Synchronize deposit method in a BankAccount class, simulate deposits from multiple threads.


## AIM:
To write a Java program that uses thread synchronization to ensure safe deposits into a shared BankAccount object when multiple threads perform deposit operations concurrently.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a BankAccount class with a balance variable.
4.	Define a synchronized deposit(int amount) method to safely update the balance.
5.	Create a DepositTask class that implements Runnable and calls the deposit method.
6.	In main(), create one shared BankAccount object.
7.	Create multiple threads (e.g., two threads) that perform deposits.
8.	Start the threads.
9.	Wait for threads to finish using join().
10.	Display the final account balance.
11.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Kasivishvanath V
RegisterNumber: 212222040073 
*/
```

## SOURCE CODE:
```
import java.util.*;

class BankAccount {
    private int balance = 0;

    public synchronized void deposit(int amount) {
        balance += amount;
    }

    public int getBalance() {
        return balance;
    }
}

class DepositThread extends Thread {
    private BankAccount account;
    private int amount;

    public DepositThread(BankAccount account, int amount) {
        this.account = account;
        this.amount = amount;
    }

    public void run() {
        account.deposit(amount);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        BankAccount account = new BankAccount();
        Thread[] threads = new Thread[n];

        for (int i = 0; i < n; i++) {
            int amount = sc.nextInt();
            threads[i] = new DepositThread(account, amount);
        }

        for (int i = 0; i < n; i++) {
            threads[i].start();
        }

        for (int i = 0; i < n; i++) {
            try { threads[i].join(); } catch (Exception e) {}
        }

        System.out.println("Final Balance: " + account.getBalance());
        sc.close();
    }
}


```
## OUTPUT:
<img width="630" height="460" alt="image" src="https://github.com/user-attachments/assets/81cdb00b-0ec4-4b42-862d-531ce8ea66be" />



## RESULT:
The program successfully demonstrates synchronization.
Multiple threads deposit money into the same BankAccount safely without data corruption, and the final balance is correct.
