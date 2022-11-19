# **Chương File (Summary)**
## **Bài 19: File CRUD (Xử lí tệp)**
- Đoạn code ví dụ:
    + Tạo file:
    ```java
    import java.io.File; // For interacting with files
    import java.io.IOException; // For handling error

    public class CFile {
        public static void main(String[] args) {
            // Đọan code tạo file
            try {
                File file1 = new File("file.txt"); // Tạo object với tên file hoặc đường dẫn là ...
                if (file1.createNewFile()) { // Nếu tên file chưa tồn tại và được tạo thành công thì ...
                    System.out.println("Đã tạo tệp " + file1.getName() + " với đường dẫn là: " + file1.getAbsolutePath());
                } else { // Nếu không thì ...
                System.out.println("Tệp đã tồn tại");
                }
            } catch (IOException IOe) {
                IOe.printStackTrace(); // Hiển thị lỗi
            }
        }
    }
    ```
    + Viết vào file:
    ```java
    import java.io.FileWriter; // For writing into file
    import java.io.IOException;

    public class WFile {
        public static void main(String[] args) {
            try {
                // Tạo object cho class FileWriter và gán tên file là ...
                FileWriter file2 = new FileWriter("file.txt");
                file2.write("Hello World!"); // Viết vào file
                file2.close(); // Đóng file
            } catch (IOException IOe) {
                IOe.printStackTrace();
            }
        }
    }
    ```
    - Đọc file:
    ```java
    import java.io.File;
    import java.io.FileNotFoundException;
    import java.util.Scanner;

    public class RFile {
        public static void main(String[] args) {
            try {
                File file3 = new File("file.txt");
                Scanner sc = new Scanner(file3);
                while (sc.hasNextLine()) {
                    String data = sc.nextLine();
                    System.out.println("Nội dung bên trong là: ");
                    System.out.println(data);
                }
                sc.close();
            } catch (FileNotFoundException fnfe) {
                fnfe.printStackTrace();
            }
        }
    }
    ```
    - Xóa file:
    ```java
    import java.io.File;

    public class DFile {
        public static void main(String[] args) {
            File file4 = new File("file.txt");
            if (file4.delete()) {
                System.out.println("Đã xóa file: " + file4.getName());
            } else {
                System.out.println("Không thể xóa file.");
            }
        }
    }
    ```