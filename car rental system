import java.io.Console;
import java.util.Scanner;

public class LoginSystem {
    public static void main(String[] args) {
        final String USERNAME = "admin";
        final String PASSWORD = "12345";
        Scanner sc = new Scanner(System.in);
        Console console = System.console();

        int attempts = 0;
        boolean loggedIn = false;

        while (attempts < 3 && !loggedIn) {
            System.out.print("Enter Username: ");
            String user = sc.nextLine();

            String pass;
            if (console != null) {
                // Mask password input as *
                char[] passwordArray = console.readPassword("Enter Password: ");
                pass = new String(passwordArray);
            } else {
                // Fallback if Console not available
                System.out.print("Enter Password: ");
              
pass = new String(passwordArray);
            } else {
                // Fallback if Console not available
                System.out.print("Enter Password: ");
                pass = sc.nextLine();
            }

            if (user.equals(USERNAME) && pass.equals(PASSWORD)) {
                System.out.println(" Login Successful!");
                loggedIn = true;
            } else {
                System.out.println(" Invalid Username or Password.");
                attempts++;
            }
        }
        if (!loggedIn) {
            System.out.println(" Access Denied! Too many attempts.");
        }
    }
}
