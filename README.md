# QuizGame-IT-23010
import java.util.Scanner;

public class QuizGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int score = 0;

        String[] questions = {
            "What is the capital of Bangladesh? (a) Dhaka (b) London (c) Rome",
            "What is 7*6? (a) 14 (b) 42 (c) 256",
            "What is 5 + 3? (a) 5 (b) 8 (c) 10",
            "What is 987654321*0? (a) 8765456789 (b) 0 (c) 2345678975",
            "What is 13*13? (a) 4 (b) 169 (c) 625"
        };

        char[] answers = {'a', 'b', 'b', 'b', 'b'};

        System.out.println("Welcome to the Quiz Game!");
        System.out.println("You will earn 5 points for each correct answer and lose 1 point for a wrong answer.");
        System.out.println("Type the letter corresponding to your answer. Let's start!\n");

        for (int i = 0; i < questions.length; i++) {
            System.out.println("Question " + (i + 1) + ": " + questions[i]);
            System.out.print("Your answer: ");
            char userAnswer = scanner.next().toLowerCase().charAt(0);

            if (userAnswer == answers[i]) {
                System.out.println("Correct!\n");
                score += 5;
            } else {
                System.out.println("Wrong! The correct answer was: " + answers[i] + "\n");
                score -= 1;
            }
        }
        System.out.println("Quiz Over! Your final score is: " + score);
        scanner.close();
    }
}
