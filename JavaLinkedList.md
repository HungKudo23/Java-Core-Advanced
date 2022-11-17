# **Chương Package (Summary)**
## **Bài 13: LinkedList (Mảng kết hợp)**
- Đoạn code ví dụ:
```java
import java.util.LinkedList; // For using dynamic array same with ArrayList
import java.util.Collections; // For using sort() method to manipulate array elements

public class Main {
    public static void main(String[] args) {
        LinkedList<Integer> myNumbers = new LinkedList<Integer>();
        // Thêm giá trị vào mảng
        myNumbers.add(10);
        myNumbers.add(15);
        myNumbers.add(20);
        myNumbers.add(25);
        // Đếm xem mảng có bao nhiêu phần tử
        myNumbers.size();
        System.out.println(myNumbers); // Kết quả: 4

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
- So sánh với `ArrayList`:
    + Giống nhau:
        + Nếu so đoạn code này với đoạn code ở bài về `ArrayList` thì sẽ thấy gần như chẳng có gì khác biệt ngoài cách khai báo. Lí do cho sự giống nhau này là vì cả 2 đều cùng triển khai giao diện `List` nên cả 2 đều có thể sử dụng tất cả phương thức của giao diện `List`
    + Khác nhau:
        + `ArrayList` sẽ nên được dùng để lưu trữ và truy cập phần tử bên trong mảng.
        + `LinkedList` sẽ nên được dùng để thao tác với phần tử trong mảng

- Phương thức phổ biến của `LinkedList`:
    + `addFirst()`: Thêm item vào đầu mảng.
    + `addLast()`: Thêm item vào cuối mảng.
    + `removeFirst()`: Xóa item ở đầu mảng.
    + `removeLast()`: Xóa item ở cuối mảng.
    + `getFirst()`: Lấy item ở đầu mảng.
    + `getLast()`: Lấy item ở cuối mảng.