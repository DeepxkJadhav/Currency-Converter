import java.util.Scanner;

public class CurrencyConverter {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("Welcome to the Currency Converter!");
        System.out.println("1. Convert USD to INR");
        System.out.println("2. Convert EUR to USD");
        System.out.print("Choose an option (1 or 2): ");
        
        int choice = scanner.nextInt();
        
        final double usdToInrRate = 83.50; 
        final double eurToUsdRate = 1.05; 
        
        if (choice == 1) {
            System.out.print("Enter amount in USD: ");
            double usd = scanner.nextDouble();
            double inr = usd * usdToInrRate;
            System.out.printf("Amount in INR: %.2f\n", inr);
        } else if (choice == 2) {
            System.out.print("Enter amount in EUR: ");
            double eur = scanner.nextDouble();
            double usd = eur * eurToUsdRate;
            System.out.printf("Amount in USD: %.2f\n", usd);
        } else {
            System.out.println("Invalid choice. Please run the program again.");
        }
        
        scanner.close();
    }
}
