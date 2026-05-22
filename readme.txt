import java.util.Random;
import java.util.Scanner;

public class GuessTheNumber {
    public static void main(String[] args) {
        Random random = new Random();
        Scanner scanner = new Scanner(System.in);

        int secretNumber = random.nextInt(100) + 1; // число від 1 до 100
        int guess;
        int attempts = 0;

        System.out.println("Я загадав число від 1 до 100. Спробуй вгадати!");

        do {
            System.out.print("Твоя відповідь: ");
            guess = scanner.nextInt();
            attempts++;

            if (guess > secretNumber) {
                System.out.println("Занадто велике число!");
            } else if (guess < secretNumber) {
                System.out.println("Занадто маленьке число!");
            } else {
                System.out.println(" Вітаю! Ти вгадав число за " + attempts + " спроб!");
            }

        } while (guess != secretNumber);

        scanner.close();
    }
}