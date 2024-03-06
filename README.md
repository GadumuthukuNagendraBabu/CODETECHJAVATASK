# CODETECHJAVATASK
Codetech_task
/**
 * This program provides a simple calculator functionality to perform basic arithmetic operations such as addition, subtraction, multiplication, and division.
 * It prompts the user to select an operation from the menu and then input two numbers to perform the selected operation.
 * After performing the operation, the program asks the user if they want to continue or exit.
 * The program runs in a loop until the user chooses to exit.
 */
package basics;

import java.util.Scanner;

public class Cal {

    /**
     * The main method of the program.
     * It displays a menu of operations, reads user input, and performs the selected operation.
     * After each operation, it prompts the user to continue or exit.
     * The program continues to run until the user chooses to exit.
     * @param args The command-line arguments passed to the program (not used in this program).
     */
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int d = 1; // Variable to control continuation of the program
        do {
            // Display menu options
            System.out.println("1.ADD\n2.SUB\n3.MUL\n4.DIV");
            System.out.println("Select the function");

            // Read user input for selected operation
            int fun = sc.nextInt();
            if (fun > 4 || fun < 1)
                System.out.println("--------Invalid--------\n------Try again--------");
            else {
                // Read two numbers from the user
                System.out.println("Enter a number");
                long a = sc.nextLong();
                System.out.println("Enter a number");
                long b = sc.nextLong();

                // Perform selected operation
                switch (fun) {
                    case 1:
                        add(a, b);
                        break;

                    case 2:
                        sub(a, b);
                        break;

                    case 3:
                        mul(a, b);
                        break;

                    case 4:
                        div(a, b);
                        break;
                    default:
                        System.out.println("Invalid ");
                }

                // Ask user if they want to continue or exit
                System.out.println("Press 1 to continue\nPress any other key to exit");
                d = sc.nextInt();
            }

        } while (d == 1); // Continue loop if user wants to continue
    }

    /**
     * Method to perform addition of two numbers and print the result.
     * @param a The first number.
     * @param b The second number.
     */
    private static void add(long a, long b) {
        System.out.println("Addition of " + a + " and " + b + " is " + (a + b));
    }

    /**
     * Method to perform subtraction of two numbers and print the result.
     * @param a The first number (minuend).
     * @param b The second number (subtrahend).
     */
    private static void sub(long a, long b) {
        System.out.println("Subtraction of " + a + " and " + b + " is " + (a - b));
    }

    /**
     * Method to perform multiplication of two numbers and print the result.
     * @param a The first number.
     * @param b The second number.
     */
    private static void mul(long a, long b) {
        System.out.println("Multiplication of " + a + " and " + b + " is " + (a * b));
    }

    /**
     * Method to perform division of two numbers and print the result.
     * If the denominator is zero, it prints an error message

