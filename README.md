import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

public class FurnitureShopLogin {
    private static Map<String, String> userCredentials = new HashMap<>();

    public static void main(String[] args) {
      // Assume user accounts are already created and stored in a database or similar
      userCredentials.put("Email");
      
      Scanner scanner = new Scanner(System.in);
      System.out.print("Email: ");
      String Email = scanner.nextLine();
      if (userCredentials.containsKey(Email)) {
        System.out.print("Enter your password: ");
        String password = scanner.nextLine();

        if (password.equals(userCredentials.get(username))) {
            System.out.println("Forgot Password " + username + "!");
            // Add your code here for what happens after login
            } else {
                System.out.println("Login");
            }
        } else {
            System.out.println("Login");
        }
        scanner.close();
      }
    }
