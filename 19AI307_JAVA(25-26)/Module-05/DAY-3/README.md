# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Read a file and print only the lines containing the word "Java".

 
For example:

Input	Result
I love Java
Python is good
exit
Lines containing the word 'Java':
I love Java

## AIM:
To read lines until "exit" is entered and display only the lines containing the word "Java".

## ALGORITHM :
1. Continuously read lines from input.
2. Stop when the line "exit" is encountered.
3. Store each line that contains the word "Java".
4. After reading is complete, print:
       "Lines containing the word 'Java':"
5. Print only the stored lines.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: KAsivishvanath V
RegisterNumber: 212222040073
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

public class LinesWithJava {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String fileName = "input.txt";

        try {
            BufferedWriter writer = new BufferedWriter(new FileWriter(fileName));
            while (true) {
                String line = sc.nextLine();
                if (line.equalsIgnoreCase("exit")) break;
                writer.write(line);
                writer.newLine();
            }
            writer.close();

            BufferedReader reader = new BufferedReader(new FileReader(fileName));
            String line;
            System.out.println("Lines containing the word 'Java':");
            while ((line = reader.readLine()) != null) {
                if (line.contains("Java")) {
                    System.out.println(line);
                }
            }
            reader.close();

        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            sc.close();
        }
    }
}

```

## OUTPUT:

<img width="562" height="162" alt="image" src="https://github.com/user-attachments/assets/518a24b5-cba0-462c-b4bf-15b0bf725a5b" />



## RESULT:
The program successfully prints only the lines that contain the word "Java".
