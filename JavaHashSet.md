# **Chương Package (Summary)**
## **Bài 14: HashSet**
- Là một collection chỉ chứa các giá trị duy nhất
- Đoạn code ví dụ
```java
import java.util.HashSet;

public class Main {
  public static void main(String[] args) {

    // Tạo object HashSet
    HashSet<Integer> numbers = new HashSet<Integer>();

    // Thêm giá trị cho set
    numbers.add(4);
    numbers.add(7);
    numbers.add(8);

    // Kiểm tra xem có số nào trong set
    for (int i = 1; i <= 10; i++) {
      if (numbers.contains(i)) { // Nếu có số nào trong set nằm trong khoảng này thì ...
        System.out.println("Số " + i + " nằm ở trong set này.");
      } else {
        System.out.println("Số " + i + " không nằm ở trong set này.");
      }
    }
  }
}
```

Kết quả:
```
Số 1 không nằm ở trong set này.
Số 2 không nằm ở trong set này.
Số 3 không nằm ở trong set này.
Số 4 nằm ở trong set này.
Số 5 không nằm ở trong set này.
Số 6 không nằm ở trong set này.
Số 7 nằm ở trong set này.
Số 8 nằm ở trong set này.
Số 9 không nằm ở trong set này.
Số 10 không nằm ở trong set này.
```
- Hàm thường dùng của HashSet:
    + `contains()`: Kiểm tra nếu giá trị đó có xuất hiện trong set hoặc không
    + `remove()`: Xóa giá trị chỉ định.
    + `clear()`: Xóa tất cả giá trị.
    + `size()`: Kiểm tra xem có bao nhiêu giá trị trong set