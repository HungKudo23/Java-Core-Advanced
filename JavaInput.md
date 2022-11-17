# **Chương Package (Summary)**
## **Bài 11: User Input (Đầu vào người dùng)**
- Đoạn code ví dụ:
```java
import java.util.Scanner; // For user input

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter your name: ");
        String name = sc.nextLine();
        System.out.println("Your name is: " + name);
        sc.close();
    }
}
```
-> Chạy đoạn code:
```
Enter your name:
Hung
Your name is: Hung
```

* Giải thích nhanh đoạn code:
  + Đầu tiên sẽ import class `Scanner` từ package **`java.util`** để lấy dữ liệu đầu vào của người dùng.
  + Tiếp theo sẽ khai báo đối tượng `sc` cho class `Scanner` trong hàm **`main`** bằng câu lệnh , rồi truyền câu lệnh `System.in` có sẵn trong class `Scanner` vào đối tượng `sc` để sử dụng.
  + Khai báo biến `name` để lưu lại dữ liệu đầu vào bằng phương thức `nextLine()` có sẵn trong class `Scanner`.
  + Sau đó dùng lệnh output để in ra dữ liệu có trong biến `name`.
  + Cuối cùng đóng khả năng truyền dữ liệu đầu vào bằng phương thức `close()` của class `Scanner` để tránh truyền nhâ

* Kiểu dữ liệu đầu vào:
  + `nextBoolean()`: Đọc theo dữ liệu kiểu `boolean`.
  + `nextByte()`: Đọc theo dữ liệu kiểu `byte`.
  + `nextDouble()`: Đọc theo dữ liệu kiểu `double`.
  + `nextFloat()`: Đọc theo dữ liệu kiểu `float`.
  + `nextInt()`: Đọc theo dữ liệu kiểu `int`.
  + `nextLine()`: Đọc theo dữ liệu kiểu `String`.
  + `nextLong()`: Đọc theo dữ liệu kiểu `long`.
  + `nextShort()`: Đọc theo dữ liệu kiểu `short`.

