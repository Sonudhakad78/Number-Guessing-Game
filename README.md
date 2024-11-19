# Number-Guessing-Game

import java.util.Scanner;
import java.util.Random;

public class NumberGuessingGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random rand= new Random();

        int RandomNumber = rand.nextInt(100)+1;
        int attempts=0;
        int guess;


        System.out.println("Welcome to the number guessing game!");
        do {
            System.out.println("Please enter a number between 1 and 100");
             guess = scanner.nextInt();
             attempts++;

             if (guess<RandomNumber){
                System.out.println("number is greater than the number you guessed!");

            }
            else if (guess>RandomNumber){
                System.out.println("number is less than the number you guessed!");
            }
                else {
                    System.out.println("Congratulations! You guessed the number in " + attempts + " attempts.");
                }

        }
        while (guess!=RandomNumber);
        scanner.close();

    }
}
