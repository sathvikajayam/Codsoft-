import java.util.Random;
import java.util.Scanner;

public class NumberGuessingGame {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Random random = new Random();
        
        int lowerBound = 1;
        int upperBound = 100;
		int attempts = 0;
        int maxAttempts = 5;
        int score = 100;
        
		boolean playAgain = true;
		
        System.out.println("Welcome to the Number Guessing Game!");
        
        while (playAgain) {
			int Number = random.nextInt(upperBound - lowerBound + 1) + lowerBound;
			System.out.println("I have selected a number between " + lowerBound + " and " + upperBound + ".");
			for(attempts=1;attempts<=maxAttempts;attempts++){
                System.out.println("Attempt " + attempts);
                System.out.print("Enter your guess :");
                int guess = sc.nextInt();
            
                if (guess < Number) {
                    System.out.println("The number is higher than "+guess);
                } 
                else if (guess > Number) {
                    System.out.println("The number is lower than "+guess);
                } 
                else {
                    System.out.println("Congratulations! You have guessed the correct number: " + Number);
                    break;
                }
                score -= 20;
				
				if (attempts == maxAttempts) {
                    System.out.println("Sorry, you have used all your attempts.");
                    System.out.println("The number was: " + Number);
                }
			}
			System.out.println("Your score: " + score);
			
			System.out.print("Do you want to play again? (yes/no): ");
            String playAgainInput = sc.next();
            playAgain = playAgainInput.equalsIgnoreCase("yes");
        }
       
        System.out.println("Thanks for playing");
        sc.close();
    }
}
