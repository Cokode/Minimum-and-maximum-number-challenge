# Minimum-and-maximum-number-challenge

import java.util.Scanner;

public class Exercises {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int min = 0;
        int max = 0;

        while(true){
            System.out.println("Enter number:");
            boolean hasAnInt = scanner.hasNextInt();
            if(hasAnInt) {
                int input = scanner.nextInt();
                if(input > max && min == 0){
                    max = input;
                    min = input;
                } else if(input >= max && input > min) {
                        max = input;
                    } else {
                    if(input < min && input > 0) min = input;
                    continue;
                }
            } else {
                System.out.println("You have entered an invalid Number!");
                break;
            }
            scanner.nextLine(); // handle inputs
        }
        System.out.println("Maximum number is: " + max + ", and Minimum number is: " + min );
        scanner.close();
    }
}
