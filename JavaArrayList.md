# **Chương Package (Summary)**
## **Bài 12: ArrayList (Mảng kết hợp)**
- Đoạn code ví dụ:
```java
import java.util.ArrayList; // For using dynamic array
import java.util.Collections; // For using sort() method to manipulate array elements

public class Main {
    public static void main(String[] args) {
        ArrayList<Integer> myNumbers = new ArrayList<Integer>();
        // Thêm giá trị vào mảng
        myNumbers.add(10);
        myNumbers.add(15);
        myNumbers.add(20);
        myNumbers.add(25);
        
        // Đếm xem mảng có bao nhiêu phần tử
        System.out.println(myNumbers.size()); // Kết quả: 4

        // Lấy giá trị của index chỉ định trong mảng
        System.out.println(myNumbers.get(3)); //  Kết quả: 25

        // Sắp xếp phần tử của mảng theo thứ tự chữ cái hoặc số
        Collections.sort(myNumbers);
        System.out.println(myNumbers); // Kết quả: 10 15 20 25

        // Thay đổi giá trị của một index bất kì trong mảng
        myNumbers.set(0, 30);
        System.out.println(myNumbers); // Kết quả: 10 15 20 30

        // Xóa một index bất kì trong mảng
        myNumbers.remove(1);
        System.out.println(myNumbers); // Kết quả: 10 20 30
        
        // Xóa toàn bộ index của mảng
        myNumbers.clear();
        System.out.println(myNumbers); // Kết quả: []
    }
}
```
- Note: 
    + Vì trong ArrayList mặc định Java sẽ hiểu các kiểu dữ liệu dưới dạng object nên nếu muốn chỉ định kiểu dữ liệu cho mảng ArrayList thì phải chỉ định kiểu dữ liệu dưới dạng object như `String`, `Integer` (thay vì `int`), `Character` (thay vì `char`), vv. <br><br>
    Chi tiết hơn có thể tham khảo bài về Wrapper Classes tại link:
    [https://www.w3schools.com/java/java_wrapper_classes.asp](https://www.w3schools.com/java/java_wrapper_classes.asp)
