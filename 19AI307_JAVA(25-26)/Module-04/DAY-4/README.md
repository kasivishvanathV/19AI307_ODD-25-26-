# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create a program that sends different types of notifications: "email", "sms", and "push". Use the Factory Pattern to generate the appropriate notification sender and call its notifyUser() method.

For example:

Input	Result
email
exit
Sending Email Notification


## AIM:
To implement the Factory Pattern that selects and returns the correct Notification object based on user input.

## ALGORITHM :
1. Create an interface Notification with notifyUser() method.
2. Create classes:
       - EmailNotification
       - SMSNotification
       - PushNotification
   Each implements notifyUser().
3. Create NotificationFactory with a method getNotification(type):
       - If type = email → return EmailNotification object
       - If type = sms → return SMSNotification
       - If type = push → return PushNotification
       - Else return null
4. In main():
       - Continuously read user input.
       - If input = exit → stop
       - Call factory to get notification object.
       - If null → print "Invalid notification type"
       - Else call notifyUser()






## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Kasivishvanath V
RegisterNumber: 212222040073
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Notification {
    void notifyUser();
}

class EmailNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Email Notification");
    }
}

class SMSNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending SMS Notification");
    }
}

class PushNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Push Notification");
    }
}

class NotificationFactory {
    public Notification createNotification(String type) {
        switch (type.toLowerCase()) {
            case "email": return new EmailNotification();
            case "sms": return new SMSNotification();
            case "push": return new PushNotification();
            default: return null;
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        NotificationFactory factory = new NotificationFactory();
        while (true) {
            String input = sc.nextLine();
            if (input.equalsIgnoreCase("exit")) break;
            Notification n = factory.createNotification(input);
            if (n != null) n.notifyUser();
            else System.out.println("Invalid notification type: " + input);
        }
    }
}

```

## OUTPUT:
<img width="400" height="152" alt="image" src="https://github.com/user-attachments/assets/0f2c281e-b993-4770-9234-af94035dd718" />



## RESULT:
The program successfully uses the Factory Pattern to generate different notification types.
