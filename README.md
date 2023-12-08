# raj-gupta
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("Enter the number of subjects:");
        int numSubjects = scanner.nextInt();
        
        double totalMarks = 0;

        for (int i = 1; i <= numSubjects; i++) {
            System.out.println("Enter marks for subject " + i + ":");
            double marks = scanner.nextDouble();
            totalMarks += marks;
        }

        double average = totalMarks / numSubjects;
        System.out.println("Average marks: " + average);
        
        char grade = calculateGrade(average);
        System.out.println("Your grade is: " + grade);
        
        scanner.close();
    }

    public static char calculateGrade(double average) {
        if (average >= 90) {
            return 'A';
        } else if (average >= 80) {
            return 'B';
        } else if (average >= 70) {
            return 'C';
        } else if (average >= 60) {
            return 'D';
        } else {
            return 'F';
        }
    }
}

