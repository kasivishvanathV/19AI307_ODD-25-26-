# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).


## AIM:
To implement a composition relationship between Library and Book classes where Book objects cannot exist independently of Library.

## ALGORITHM :
1.Create Book class with title, author attributes
2.Create Library class that contains and manages Book objects
3.Instantiate Book objects only inside Library methods
4.Ensure Book objects are destroyed when Library is destroyed
5.Demonstrate composition relationship



## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Kasivishvanath V
RegisterNumber:  212222040073
*/
```

## SOURCE CODE:
```
import java.util.*;

class Book {
    private String title;
    private String author;
    
    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }
    
    public String getBookInfo() {
        return "- " + title + " by " + author;
    }
}

class Library {
    private List<Book> books;
    
    public Library() {
        books = new ArrayList<>();
    }
    
    public void addBook(String title, String author) {
        Book book = new Book(title, author);
        books.add(book);
    }
    
    public void displayBooks() {
        System.out.println("Books in Library:");
        for (Book book : books) {
            System.out.println(book.getBookInfo());
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        int n = scanner.nextInt();
        scanner.nextLine();
        
        Library library = new Library();
        
        for (int i = 0; i < n; i++) {
            String title = scanner.nextLine();
            String author = scanner.nextLine();
            library.addBook(title, author);
        }
        
        library.displayBooks();
        
        scanner.close();
    }
}
```






## OUTPUT:
<img width="831" height="479" alt="image" src="https://github.com/user-attachments/assets/1c0f134c-cb3c-46d3-9a74-0fb4698b270c" />



## RESULT:
The composition relationship was successfully implemented. Book objects were created only within the Library class and could not exist independently, demonstrating proper composition where child objects have no existence without the parent object.
