# Grade_Statistics
import java.util.Scanner;

public class Grade {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double total = 0.0;
        Double maximum = null;
        Double minimum = null;

        for (int i = 1; i <= 10; i++) {
            double grade;
            while (true) {
                try {
                    System.out.print("Enter grade " + i + ": ");
                    grade = Double.parseDouble(scanner.nextLine());
                    break;
                } catch (NumberFormatException e) {
                    System.out.println("Invalid input. Please enter a valid floating-point number.");
                }
            }

            total += grade;

            if (maximum == null || grade > maximum) {
                maximum = grade;
            }
            if (minimum == null || grade < minimum) {
                minimum = grade;
            }
        }

        double average = total / 10;

        System.out.println("Average grade: " + average);
        System.out.println("Maximum grade: " + maximum);
        System.out.println("Minimum grade: " + minimum);
    }
}
