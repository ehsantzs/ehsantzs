import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String[] names = new String[10];

        System.out.println("Please Enter 10 Name:");
        for (int i = 0; i < 10; i++) {
            System.out.print("Name " + (i + 1) + ": ");
            names[i] = scanner.nextLine();
        }

        System.out.println("\nOutput:");
        for (String name : names) {
            int length = name.length();
            System.out.println("Name: " + name + " = Word count: " + length + " ❤️");
        }

        scanner.close();
    }
}
