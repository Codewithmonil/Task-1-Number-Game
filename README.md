import java.util.Random;
import java.util.Scanner;

public class NumberGame {
    public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);
                    Random random = new Random();
        int minRange = 1;
                int maxRange = 100;
                        int numberOfAttempts = 10;
                                int score = 0;
        boolean playAgain = true;
        while (playAgain) {
                    int targetNumber = random.nextInt(maxRange - minRange + 1) + minRange;
                                System.out.println("Welcome to the Number Guessing Game!");
                                            System.out.println("I'm thinking of a number between " + minRange + " and " + maxRange);
            for (int attempts = 1; attempts <= numberOfAttempts; attempts++) {
                            System.out.print("Enter your guess (" + attempts + "/" + numberOfAttempts + "): ");
                                            int userGuess = scanner.nextInt();
                if (userGuess == targetNumber) {
                                    System.out.println("Congratulations! You guessed the correct number: " + targetNumber);
                    score++;
     break;
     } 
     else if (userGuess < targetNumber) {
                                                                                                                System.out.println("Try a higher number.");
                                                                                                                                } 
                                                                                                                                else {
                                                                                                                                                    System.out.println("Try a lower number.");
                                                                                                                                                                    }
                if (attempts == numberOfAttempts) {
                                    System.out.println("You've run out of attempts. The correct number was: " + targetNumber);
                                                    }
                                                                }
            System.out.print("Do you want to play again? (yes/no): ");
                        String playAgainResponse = scanner.next();
                                    playAgain = playAgainResponse.equalsIgnoreCase("yes");
                                            }
        System.out.println("Thank you for playing! Your total score is: " + score);
            }
            }
