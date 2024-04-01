import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

public class UpdateAccountDetailsExample {
    private static Map<String, UserDetails> userMap = new HashMap<>();
public static void main(String[] args) {
        // Assume user accounts are already created and stored in a database or similar
        
Scanner scanner = new Scanner(System.in);
        System.out.print("Enter your username: ");
        String username = scanner.nextLine();

        if (userMap.containsKey(username)) {
            UserDetails userDetails = userMap.get(username);
System.out.println("Current Details:");
            System.out.println("First Name: " + userDetails.getFirstName());
            System.out.println("Last Name: " + userDetails.getLastName());
            System.out.println("Phone Number: " + userDetails.getPhoneNumber());
            System.out.println("Email Address: " + userDetails.getEmailAddress());
            System.out.println("Postcode: " + userDetails.getPostcode());
System.out.println("\nEnter new details:");

            System.out.print("First Name: ");
            String newFirstName = scanner.nextLine();

            System.out.print("Last Name: ");
            String newLastName = scanner.nextLine();

            System.out.print("Phone Number: ");
            String newPhoneNumber = scanner.nextLine();
          System.out.print("Email Address: ");
            String newEmailAddress = scanner.nextLine();

            System.out.print("Postcode: ");
            String newPostcode = scanner.nextLine();

            // Update the user details in the map (simulate database update)
            userDetails.setFirstName(newFirstName);
            userDetails.setLastName(newLastName);
            userDetails.setPhoneNumber(newPhoneNumber);
            userDetails.setEmailAddress(newEmailAddress);
            userDetails.setPostcode(newPostcode);
   System.out.println("\nDetails updated successfully.");
        } else {
            System.out.println("User not found.");
        }

        scanner.close();
    }

    static class UserDetails {
        private String firstName;
        private String lastName;
        private String phoneNumber;
        private String emailAddress;
        private String postcode;
         public UserDetails(String firstName, String lastName, String phoneNumber, String emailAddress, String postcode) {
            this.firstName = firstName;
            this.lastName = lastName;
            this.phoneNumber = phoneNumber;
            this.emailAddress = emailAddress;
            this.postcode = postcode;
        }
         public String getFirstName() {
            return firstName;
        }

        public void setFirstName(String firstName) {
            this.firstName = firstName;
        }

        public String getLastName() {
            return lastName;
        }
 public void setLastName(String lastName) {
            this.lastName = lastName;
        }

        public String getPhoneNumber() {
            return phoneNumber;
        }

        public void setPhoneNumber(String phoneNumber) {
            this.phoneNumber = phoneNumber;
        }
public String getEmailAddress() {
            return emailAddress;
        }

        public void setEmailAddress(String emailAddress) {
            this.emailAddress = emailAddress;
        }

        public String getPostcode() {
            return postcode;
        }

        public void setPostcode(String postcode) {
            this.postcode = postcode;
        }
    }

    
        
   
