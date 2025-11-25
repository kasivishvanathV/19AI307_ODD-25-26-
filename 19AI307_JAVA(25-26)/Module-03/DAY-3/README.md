# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class GameScore with method finalScore().
Subclasses:

ArcadeGame: score = baseScore + (level × 100)

PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

Input Format:

First line: 1 or 2
Second line: base, level (or attempts)

Output Format:

Final score (int)

## AIM:
To write a Java program that defines an abstract class GameScore with an abstract method finalScore(), and implements two subclasses ArcadeGame and PuzzleGame to calculate the final score based on given rules.

## ALGORITHM :
1.	Start the program.
2.	Create an abstract class GameScore with an abstract method finalScore().
3.	Create subclasses ArcadeGame and PuzzleGame implementing their own scoring formulas.
4.	Read input from the user and create the appropriate subclass object.
5.	Call finalScore() and print the result.
	
## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Kasivishvanath V
RegisterNumber: 212222040073
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

abstract class GameScore {
    abstract int finalScore();
}

class ArcadeGame extends GameScore {
    int baseScore, level;
    ArcadeGame(int baseScore, int level) {
        this.baseScore = baseScore;
        this.level = level;
    }
    int finalScore() {
        return baseScore + (level * 100);
    }
}

class PuzzleGame extends GameScore {
    int attempts;
    PuzzleGame(int attempts) {
        this.attempts = attempts;
    }
    int finalScore() {
        return (attempts <= 3) ? 1000 - (attempts * 100) : 500;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int gameType = sc.nextInt();
        GameScore game;
        if (gameType == 1) {
            int base = sc.nextInt();
            int level = sc.nextInt();
            game = new ArcadeGame(base, level);
        } else {
            int attempts = sc.nextInt();
            game = new PuzzleGame(attempts);
        }
        System.out.println(game.finalScore());
        sc.close();
    }
}

```
## OUTPUT:
<img width="454" height="323" alt="image" src="https://github.com/user-attachments/assets/e2cb0d31-def4-4495-8144-b3092d311efd" />



## RESULT:
The program successfully implements an abstract class GameScore and its subclasses ArcadeGame and PuzzleGame, calculates the final score based on user input, and displays the correct final score according to the defined scoring rules.
