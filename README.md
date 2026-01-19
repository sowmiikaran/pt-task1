import java.util.InputMismatchException;
import java.util.Scanner;

public class PRODIGY_SD_01 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            System.out.print("Enter temperature value: ");
            double temperature = scanner.nextDouble();
            scanner.nextLine(); // consume end-of-line

            System.out.print("Enter original unit (C for Celsius, F for Fahrenheit, K for Kelvin): ");
            String unitInput = scanner.nextLine().trim();
            if (unitInput.isEmpty()) {
                System.out.println("No unit provided. Exiting.");
                return;
            }

            char originalUnit = Character.toUpperCase(unitInput.charAt(0));
            convertAndDisplay(temperature, originalUnit);
        } catch (InputMismatchException e) {
            System.out.println("Invalid temperature. Please enter a numeric value.");
        } finally {
            scanner.close();
        }
    }

    private static void convertAndDisplay(double temperature, char originalUnit) {
        double celsius;

        switch (originalUnit) {
            case 'F':
                celsius = (temperature - 32.0) * 5.0 / 9.0;
                break;
            case 'K':
                celsius = temperature - 273.15;
                break;
            case 'C':
                celsius = temperature;
                break;
            default:
                System.out.println("Unknown unit. Please use C, F, or K.");
                return;
        }

        double fahrenheit = (celsius * 9.0 / 5.0) + 32.0;
        double kelvin = celsius + 273.15;

        System.out.println("Converted Temperatures:");
        System.out.printf("Celsius: %.2f%n", celsius);
        System.out.printf("Fahrenheit: %.2f%n", fahrenheit);
        System.out.printf("Kelvin: %.2f%n", kelvin);
    }
}
