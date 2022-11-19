# **Chương Package (Summary)**
## **Bài 15: Iterator (Trình lặp lại)**
- Là một object thực hiện việc lặp lại (giống như vòng lặp) thông qua collection.
- Đoạn code ví dụ:
```java
import java.util.ArrayList; // For using ArrayList
import java.util.Iterator; // For using Iterator

public class Main {
  public static void main(String[] args) {

    // Tạo một collection
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");

    // Lấy Iterator bằng cách nối collection với hàm iterator()
    Iterator<String> it = cars.iterator();

    // In ra tất cả giá trị trong collection
    while (it.hasNext()) { // Nếu trong collection còn giá trị sau giá trị đầu..
      System.out.println(it.next()); // Hiển thị tất cả giá trị của collection cho đến hết 
    }
  }
}
```
Kết quả:
```
Volvo
BMW
Ford
Mazda
```
- Hàm có sẵn của Iterator:
    + `iterator()`: Dùng để lấy Iterator từ một collection.
    + `hasNext()`: Kiểm tra nếu trong iterator có phần tử bên trong 
    + `next()`: Trả về giá trị xuất hiện kế tiếp có trong vòng lặp.
    + `remove()`: Dùng để loại bỏ giá trị (chỉ có tác dụng khi thực hiện vòng lặp `while`) 