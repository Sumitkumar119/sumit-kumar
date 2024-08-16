import java.util.Scanner;

public class Login {
    private static String username = "admin";
    private static String password = "password";

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter username:");
        String inputUsername = scanner.nextLine();
        System.out.println("Enter password:");
        String inputPassword = scanner.nextLine();

        if (inputUsername.equals(username) && inputPassword.equals(password)) {
            System.out.println("Login successful!");
            menu();
        } else {
            System.out.println("Invalid username or password. Please try again.");
            main(args);
        }
    }

    private static void menu() {
        System.out.println("Select an option:");
        System.out.println("1. Update Profile and Password");
        System.out.println("2. Selecting answers for MCQs");
        System.out.println("3. Logout");
        Scanner scanner = new Scanner(System.in);
        int option = scanner.nextInt();

        switch (option) {
            case 1:
                updateProfileAndPassword();
                break;
            case 2:
                mcqs();
                break;
            case 3:
                logout();
                break;
            default:
                System.out.println("Invalid option. Please try again.");
                menu();
        }
    }

    private static void updateProfileAndPassword() {
        // Update profile and password logic here
        System.out.println("Update profile and password functionality not implemented.");
        menu();
    }

    private static void mcqs() {
        // MCQs logic here
        System.out.println("MCQs functionality not implemented.");
        menu();
    }

    private static void logout() {
        System.out.println("Logging out...");
        main(new String[0]);
    }
}
