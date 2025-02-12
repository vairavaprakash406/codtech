import java.io.*;
import java.util.Scanner;

public class FileOperations {

    public static void readFile(String fileName) {
        try (BufferedReader reader = new BufferedReader(new FileReader(fileName))) {
            String line;
            System.out.println("Reading file: " + fileName);
            while ((line = reader.readLine()) != null) {
                System.out.println(line);
            }
        } catch (IOException e) {
            System.out.println("Error reading file: " + e.getMessage());
        }
    }

    public static void writeFile(String fileName, String content) {
        try (BufferedWriter writer = new BufferedWriter(new FileWriter(fileName))) {
            writer.write(content);
            System.out.println("Content written to file: " + fileName);
        } catch (IOException e) {
            System.out.println("Error writing to file: " + e.getMessage());
        }
    }

    public static void modifyFile(String fileName, String newContent) {
        try (BufferedWriter writer = new BufferedWriter(new FileWriter(fileName, true))) {
            writer.newLine();
            writer.write(newContent);
            System.out.println("Content appended to file: " + fileName);
        } catch (IOException e) {
            System.out.println("Error modifying file: " + e.getMessage());
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter the file name (with extension):");
        String fileName = scanner.nextLine();

        System.out.println("Choose an operation: \n1. Read File \n2. Write File \n3. Modify File");
        int choice = scanner.nextInt();
        scanner.nextLine();

        switch (choice) {
            case 1:
                readFile(fileName);
                break;

            case 2:
                System.out.println("Enter content to write to the file:");
                String content = scanner.nextLine();
                writeFile(fileName, content);
                break;

            case 3:
                System.out.println("Enter content to append to the file:");
                String newContent = scanner.nextLine();
                modifyFile(fileName, newContent);
                break;

            default:
                System.out.println("Invalid choice.");
        }

        scanner.close();
    }
}
