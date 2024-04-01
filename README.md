import java.util.Scanner;

public class LogoutExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Oh no!You're Leaving....Are You Sure)");
        String response = scanner.nextLine();
        if (response.equalsIgnoreCase("Yes")) {
            logout();
            System.out.println("No Just Kidding.");
        } else if (response.equalsIgnoreCase("No, Just Kidding")) {
            System.out.println("Yes,Logout Me");
        } else {
            System.out.println("Invalid response. Please enter 'Yes' or 'No, Just Kidding'.");
        }

    
        
    }
       
