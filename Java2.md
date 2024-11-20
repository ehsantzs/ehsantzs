import java.util.Scanner;

public class EmployeeSalary {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double[] salaries = new double[10];

        for (int i = 0; i < salaries.length; i++) {
            System.out.print("salary" + (i + 1)+": ");
            salaries[i] = scanner.nextDouble();
        }

        System.out.println("\n after calculations:");
        for (int i = 0; i < salaries.length; i++) {
            double salary = salaries[i];

            if (salary > 5800000) {
                double insuranceDeduction = salary * 0.05;
                salary -= insuranceDeduction;
                double childAllowance = salary * 0.07;
                salary += childAllowance;
            }

            System.out.printf("Employee salary %d: %.2f\n", (i + 1), salary);
        }

        scanner.close();
    }
}
