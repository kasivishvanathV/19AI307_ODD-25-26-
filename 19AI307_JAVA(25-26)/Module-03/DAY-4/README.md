# Ex.No:3(D)    INTERFACE 

## QUESTION:
Each judge uses different criteria to score fighters. Based on points, the judge will declare “WIN”, “LOSE” or “DRAW”.

LenientJudge: WIN if diff ≥ 5, DRAW if < 5

StrictJudge: WIN if diff ≥ 10, DRAW if < 10

Input Format:

player1Score
player2Score
judgeType
player1Score, player2Score: integers

judgeType: 1 for LenientJudge, 2 for StrictJudge

Output Format:
WIN / LOSE / DRAW

## AIM:
To write a Java program that determines the match result (WIN / LOSE / DRAW) using two judge types: LenientJudge and StrictJudge, based on the score difference between two fighters.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Read player1Score, player2Score, and judgeType from the user.
4. Based on judgeType, use LenientJudge or StrictJudge to evaluate the result.
5. Display WIN, LOSE, or DRAW according to the scoring rules.	

## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Kasivishvanath V
RegisterNumber: 212222040073
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Judge {
    String decide(int player1Score, int player2Score);
}

class LenientJudge implements Judge {
    public String decide(int player1Score, int player2Score) {
        int diff = player1Score - player2Score;
        if (diff >= 5) return "WIN";
        else if (diff <= -5) return "LOSE";
        else return "DRAW";
    }
}

class StrictJudge implements Judge {
    public String decide(int player1Score, int player2Score) {
        int diff = player1Score - player2Score;
        if (diff >= 10) return "WIN";
        else if (diff <= -10) return "LOSE";
        else return "DRAW";
    }
}

public class FightingMatch {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int player1Score = sc.nextInt();
        int player2Score = sc.nextInt();
        int judgeType = sc.nextInt();

        Judge judge;
        if (judgeType == 1) judge = new LenientJudge();
        else if (judgeType == 2) judge = new StrictJudge();
        else return;

        System.out.println(judge.decide(player1Score, player2Score));
        sc.close();
    }
}

```
## OUTPUT:
<img width="445" height="409" alt="image" src="https://github.com/user-attachments/assets/1686b08b-a6af-4d84-b7cd-48031a8aa046" />



## RESULT:
The program successfully applies the scoring rules of LenientJudge and StrictJudge based on the input score difference and outputs the correct match result: WIN, LOSE, or DRAW.
